<template>
    <section class="mx-3 d-flex flex-column flex-xl-row justify-content-between align-content-center ">
        <div class="left align-self-center">
            <h2 class="text-capitalize fw-bold fs-1">We are here to 
                Make your <span>website</span> <br>
                look more <span>elegant</span>  <br>
                and stilish!
            </h2>
            <Divider/>
            <ButtonPrimary :text="'view all'"/>
        </div>
        <div class="right align-self-center mt-5">
            <div class="row gap-5 justify-content-center">
                <Card :icon="'gauge-simple-high'" :title="'speed optimization'"/>
                <Card :icon="'cloud'" :title="'cloud solutions'"/>
                <Card :icon="'tablet-screen-button'" :title="'website design'"/>
                <Card :icon="'stopwatch'" :title="'online marketing'"/>
            </div>
        </div>
    </section>
</template>

<script>
import Divider from './Divider.vue';
import ButtonPrimary from './ButtonPrimary.vue';
import Card from './Card.vue'
    export default {
    name: 'Services',
    components: {
        Divider,
        ButtonPrimary,
            Card
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    margin: 20vh 0;
}

h2{
    span{
        color: $contrast-color;
    }
}
</style>