<template>
    <section class="m-5">
        <div class="row justify-content-between">
            <div id="email" class="shadow col-12 col-md-6 d-flex flex-column align-items-center p-5 rounded-4 w-100 shadow-sm">
                <span class="text-capitalize mb-2">are you ready</span>
                <h2 class="mb-5 fw-bold fs-1">Start a New Project</h2>
                <div class="position-relative">
                    <input type="email" placeholder="Enter Your Email Adress" class="rounded-5">
                    <button class="text-uppercase position-absolute rounded-4">submit</button>
                </div>
            </div>
            <div id="start" class="col-12 col-md-6 d-flex flex-column align-items-center p-5 rounded-4 w-100 mt-5 mt-md-0">
                <span class="text-capitalize mb-2">what are you waiting for</span>
                <h2 class="mb-5 fw-bold fs-1">Start a New Project</h2>
                <ButtonSecondary :text="'start now'"/>
            </div>
        </div>
    </section>
</template>

<script>
import ButtonSecondary from './ButtonSecondary.vue';
    export default {
    name: 'CallToAction',
    components: {
        ButtonSecondary
    }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

#email{
    background: $gradient-secondary;
    color: $bg-primary;
    height: 40vh;
    
    div{
        width: 80%;
    }
    input{
        width: 100%;
        height: 55px;
        border: none;
        padding-left: 20px;
        background: #505050;
    }
    button{
        border: none;
        background: transparent;
        height: 85%;
        color: $text-grey;
        font-weight: bold;
        right: 10px;
        top: 3px;
        &:hover{
            background: $gradient-secondary;
        }
    }
}
#start{
    background: $hover-bg-reverse;
    color: $bg-primary;
    height: 40vh;
    box-shadow: 6px 6px 25px 0 rgba(210, 64, 93,.35);

}

@media screen and (min-width: 768px){
    #email{
        width: 48% !important;
    }
    #start{
        width: 48% !important;
    }
}

</style>