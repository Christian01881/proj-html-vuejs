<template>
    <div id="main">
        <section id="intro" class="container text-center pt-4">
            <h1 class="mt-5">Welcome to Avada Health</h1>
            <p class="wrap mt-4 fs-5">set ud perspiciatis unde omnis natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo</p>
            <div class="d-flex">
                <AppSingleCard v-for="card in introSection" :card="card"/>
            </div>
        </section>
        <section id="our-doctor" class="container text-center">
            <img src="../images/" alt="">
        </section>
    </div>
</template>

<script>
import { introSection } from '../data/store';
import AppSingleCard from './AppSingleCard.vue';
    export default {
    name: "AppMain",
    data() {
        return {
            introSection
        };
    },
    components: { AppSingleCard }
}
</script>

<style lang="scss" scoped>
    .wrap{
        width: 700px;
        margin: 0 auto;
    }

    #our-doctor{
        background-color: #f7f7f7;
    }
</style>