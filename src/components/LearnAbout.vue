<template>
    <section class="d-flex flex-column flex-xl-row position-relative">
        <div class="left">
            <div id="bg-img" class="d-none d-xl-block">
                <div class="filter"></div>
            </div>
            <div class="image-container">
                <div class="upper-image"></div>
                <div class="lower-image"></div>
            </div>

        </div>
        <div class="right">
            <h2 class="fw-bold fs-1 mt-5 mt-xl-0"> learn more about <br> our <span>missions</span>  </h2>
            <Divider/>
            <p class="mb-4">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.</p>
    <ButtonPrimary :text="'read more'"/>
        </div>
    </section>
</template>

<script>
import Divider from './Divider.vue';
import ButtonPrimary from './ButtonPrimary.vue';
    export default {
    name: 'LearnAbout',
    components: {
        Divider,
            ButtonPrimary
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    height: 100vh;
    margin: 20vh 0;
    padding: 15vh;
    background-color: $bg-secondary;
    .left{
        width: 55%;
        overflow: hidden;
        #bg-img{
            position: absolute;
            z-index: 2;
            height: 70%;
            width: 45%;
            left: -100px;
            top: 40px;
            background-image: url('/images/busy-architect-PYVKWM4-1024x872.jpg');
            background-size: cover;
            border-radius: 40px;
            
            .filter{
                width: 100%;
                height: 100%;
                z-index: 5;
                background: $hover-bg;
                opacity: 80%;
                border-radius: 40px;
            }
        }

        .image-container {
            width: 600px; 
            height: 500px; 
            position: relative; 
            overflow: hidden; 
            z-index: 10;
        }

        .upper-image {
            position: absolute; 
            top: 0; 
            width: 100%; 
            height: 50%; 
            background-image: url('/images/businesswoman-analysing-document-P8WSNMC-1024x820.jpg'); 
            background-position: top center; 
            background-size: cover; 
            transform: translateX(10%); 
        }
        .lower-image {
            position: absolute; 
            bottom: 0; 
            width: 100%;
            height: 50%; 
            background-image: url('/images/businesswoman-analysing-document-P8WSNMC-1024x820.jpg'); 
            background-position: bottom center; 
            background-size: cover; 
            transform: translateX(-10%); 
        }
    }
    .right{
        width: 45%;
        h2{
            span{
                color: $contrast-color;
            }
        }
    }
    }

</style>