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
        <section id="facilities" class="text-white text-center">
            <div class="d-flex flex-column justify-content-center tour align-items-center pt-5">
                <img class="mt-3" src="../images/icon-7.png" alt="">
                <h1 class="text-uppercase py-4">tour our facilities</h1>
                <hr class="rule-2">
                <p class="paragraph pt-4">Sed ut perspicatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aprim, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae</p>
                <img class="mt-4 play pb-5" src="../images/play-icon.png" alt="">
            </div>
            <div class="sash d-flex">
                <div class="sash-1 d-flex flex-column align-items-center justify-content-center">
                    <h4>Emergency Care</h4>
                    <img class="pt-3" src="../images/wave-divider.png" alt="">
                    <p class="p-3">Sed ut perspiciatis unde iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
                    <button class="text-uppercase">Learn more</button>
                </div>
                <div class="sash-2 d-flex flex-column align-items-center justify-content-center">
                    <h4>Emergency Care</h4>
                    <img class="pt-3" src="../images/wave-divider.png" alt="">
                    <p class="p-3">Sed ut perspiciatis unde iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
                    <button class="text-uppercase">Learn more</button>
                </div>
                <div class="sash-3 d-flex flex-column align-items-center justify-content-center">
                    <h4>Emergency Care</h4>
                    <img class="pt-3" src="../images/wave-divider.png" alt="">
                    <p class="p-3">Sed ut perspiciatis unde iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
                    <button class="text-uppercase">Learn more</button>
                </div>
            </div>
            <div id="appointment" class="text-white text-center d-flex flex-column justify-content-center align-items-center">
                <h1 class="pb-4">Make an Appointment</h1>
                <hr class="rule-2">
                <p class="paragraph pt-4">Sed ut perspicatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aprim, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae</p>
                <div class="d-flex flex-wrap justify-content-between align-items-center paragraph mt-4">
                    <input  type="text" placeholder="Name*">
                    <input  type="email" placeholder="E-mail*">
                    <input class="mt-3" type="number" placeholder="Phone number">
                    <input class="mt-3" type="number" placeholder="Appointment Date*">
                    <textarea name="" id="" cols="30" rows="10" placeholder="How can we help?*"></textarea>
                    <button class="appointment text-uppercase text-white fs-5">Make an appointment</button>
                </div>
            </div>
            <div>
                <AppSlider />
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
import AppSlider from './AppSlider.vue';
    export default {
    name: "AppMain",
    data() {
        return {
            introSection,
            doctorSection,
            serviceSection
        };
    },
    components: { AppSingleCard, AppDoctorCard, AppSlider }
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
        height: 3px;
        background-color: grey;
    }

    .rule-2{
        color: white;
        width: 22%;
        height: 2px;
        background-color: white;
    }

    .icon{
        width: 80px;
    }

    .tour{
        width: 100%;
        height: 80vhvh;
        background-image: url(../images/paralax-bg-tour-facilities.jpg);
        background-size: cover;
        background-position-y: -180px;
    }

    .play{
        cursor: pointer;

        &:hover{
            scale: 1.1;
        }
    }

    .sash{
        width: 100%;
        height: 300px;

        .sash-1{
            background-color: #3aafbf;
            width: calc(100% / 3);
            height: 100%;
        }

        .sash-2{
            background-color: #3597c3;
            width: calc(100% / 3);
            height: 100%;
        }

        .sash-3{
            background-color: #327ec7;
            width: calc(100% / 3);
            height: 100%;
        }

        button{
            text-decoration: none;
            background-color: transparent;
            border: 3px solid white;
            color: white;
            padding: 6px 20px;
        }
    }

    #appointment{
        width: 100%;
        height: 100vh;
        background-image: url(../images/make-an-appointment.jpg);
        background-size: cover;
    }

    input{
        width: 48%;
        height: 30px;
        padding: 20px;
        text-decoration: none;
        background-color: transparent;
        border: 1px solid white;
        color: white;

    }

    textarea{
        margin-top: 20px;
        width: 100%;
        height: 100px;
        text-decoration: none;
        background-color: transparent;
        border: 1px solid white;
        color: white;
    }

    .appointment{
        width: 100%;
        height: 50px;
        text-decoration: none;
        background-color:#3aafbf;
        margin-top: 20px;
        border: none;
    }
</style>