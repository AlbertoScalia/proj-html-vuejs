<template>
    <section class="mx-3">
        <div class="d-flex flex-column flex-lg-row align-items-center justify-content-between">
            <div class="left">
                <Divider/>
                <h2 class="fs-1 fw-bold my-5"> Our recent <span>web designs</span>  & <br> some examples of <br> past <span>projects</span> </h2>
                <Divider/>
            </div>
            <div class="right d-flex align-items-end h-100">
                <p class="mt-5">Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.Separated they live in Bookmarksgrove.Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove.
                </p>
            </div>
        </div>
        
        <div class="row w-100 my-5">
            <ShowcaseCard v-for="item in showcase" :image="item.image" :title="item.title" :category="item.category"/>
        </div>
        <div class="text-center mb-5">
            <ButtonPrimary :text="'read more'"/>
        </div>
    </section>
</template>

<script>
import {showcase} from '../data/data'
import Divider from './Divider.vue';
import ShowcaseCard from './ShowcaseCard.vue';
import ButtonPrimary from './ButtonPrimary.vue';
    export default {
    name: 'Showcase',
    components: { Divider, ShowcaseCard , ButtonPrimary },
    data() {
        return {
                showcase
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

section{
    margin: 20vh 0;
}
.left{
    width: 45%;
    .divider{
        margin-top: 0 !important;
        margin-bottom: 0 !important;
    }
    h2{
        span{
            color: $contrast-color;
        }
    }
}
.right{
    width: 50%;
}
</style>