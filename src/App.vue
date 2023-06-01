<template>
  <HeaderComponent/>
  <MainComponent/>
  <FooterComponent/>
  <div class="back-home d-flex justify-content-center align-items-center" @click="scrollToTop">
    <a href="">
      <i class="fa-solid fa-arrow-up"></i>
    </a>
  </div>
  <div class="chat d-flex justify-content-center align-items-center">
    <i class="fa-regular fa-comment fs-5"></i>
  </div>
  <div class="d-flex flex-column options-contaner">
    <div class="options mb-2 p-2 rounded-start d-flex align-items-center">
      <i class="fa-brands fa-microsoft text-white p-2"></i>
      <span class="small text-white">Browse Demos</span>
  </div>
  <div class="options mb-2 p-2 rounded-start d-flex align-items-center">
    <i class="fa-solid fa-bag-shopping text-white p-2"></i>
    <span class="small text-white">Buy now!</span>
  </div>
  <div class="options mb-2 p-2 rounded-start d-flex align-items-center">
    <i class="fa-solid fa-arrow-right-from-bracket text-white p-2"></i>
    <span class="small text-white">Export section</span>
  </div>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
  export default {
  name: 'App',
  components: { HeaderComponent, MainComponent, FooterComponent },
    methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    }
  }
  }
</script>

<style lang="scss" scoped>
@use './assets/styles/partials/variables' as *;
.back-home{
  width: 30px;
  height: 30px;
  border-radius: 50%;
  position: fixed;
  right: 80px;
  bottom: 30px;
  border: 1px solid $icons-color;
  background-color: $bg-primary;
  transition: .5s;
  z-index: 900;
  i{
    font-size: .8rem;
  }
  &:hover{
    border: 1px solid $bg-primary;
    background-color: $icons-color;
    cursor: pointer;
    a{
      color: $bg-primary;
    }
  }

  a{
    text-decoration: none;
    color: $icons-color;
  }
}
.chat{
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: rgb(82, 124, 235);
  color: $bg-primary;
  position: fixed;
  right: 20px;
  bottom: 20px;
  transition: .5s;
  z-index: 900;
  &:hover{
    background-color: rgb(74, 116, 227);
    box-shadow: rgba(0, 0, 0, 0.06) 0px 0px 0px 30px inset;
    cursor: pointer;
  }
}

.options-contaner{
  position: fixed;
  right: 0px;
  bottom: 40%;
  z-index: 900;
}
.options{
  width: 150px;
  height: 45px;
  background-color: rgba(100, 100, 100, 0.7);
  &:hover{
    background: $hover-bg-reverse;
    box-shadow: 6px 6px 25px 0 rgba(0,217,166,.35);
    cursor: pointer;
  }
}
</style>