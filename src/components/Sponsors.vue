<template>
    <section class="my-5 py-5">
        <div class="row justify-content-center align-items-center my-5">
            <div class="col-12 col-md-4 col-lg-2 mt-5 mt-lg-0 d-flex justify-content-center py-3" v-for="sponsor in sponsors">
                <img :src="sponsor.image" :alt="sponsor.name" class="img-fluid">
            </div>
        </div>
    </section>
</template>

<script>
import {sponsors} from '../data/data'
    export default {
    name: 'Sponsors',
    data() {
        return {
                sponsors
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
section{
    background-color: $bg-secondary;
}
.row{
    height: 80px;
    .col-12{
        height: 100%;
    }
}
</style>