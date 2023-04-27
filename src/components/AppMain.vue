<template>
    <div id="main">
        <section id="intro" class="container text-center pt-4">
            <h1 class="mt-5">Welcome to Avada Health</h1>
            <p class="wrap mt-4 fs-5">set ud perspiciatis unde omnis natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo</p>
            <div class="d-flex">
                <AppSingleCard v-for="card in introSection" :card="card"/>
            </div>
        </section>
        <section id="our-doctor" class="text-center">
            <div class="container">
                <div class="d-flex flex-column align-items-center">
                    <img class="py-5 mt-5" src="../images/icon-5.png" alt="">
                    <h1 class="text-uppercase pb-3">Meet our doctor</h1>
                    <hr class="rule">
                    <p class="paragraph pt-4">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium aoloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae</p>
                </div>
                <div class="d-flex justify-content-center py-5 gap-5">
                    <AppDoctorCard v-for="card in doctorSection" :card="card"/>
                </div>
            </div>
        </section>
        <section id="service">
            <div class="container">
                <div class="d-flex flex-column align-items-center text-center">
                    <img class="py-5 mt-5 icon" src="../images/icon-6.png" alt="">
                    <h1 class="text-uppercase pb-3">Meet our doctor</h1>
                    <hr class="rule">
                    <p class="paragraph pt-4">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium aoloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae</p>
                </div>
                <div class="d-flex flex-wrap gap-3 justify-content-center text-center pb-5">
                    <AppSingleCard v-for="card in serviceSection" :card="card"/>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import { introSection } from '../data/store';
import { doctorSection } from '../data/store';
import { serviceSection } from '../data/store';
import AppDoctorCard from './AppDoctorCard.vue';
import AppSingleCard from './AppSingleCard.vue';
    export default {
    name: "AppMain",
    data() {
        return {
            introSection,
            doctorSection,
            serviceSection
        };
    },
    components: { AppSingleCard, AppDoctorCard }
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

    .paragraph{
            width: 600px;
            line-height: 30px;
        }

    .rule{
        color: grey;
        width: 22%;
        height: 2px;
        background-color: grey;
    }

    .icon{
        width: 80px;
    }
</style>