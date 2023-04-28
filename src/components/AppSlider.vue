<template>
    <div class="slider">
        <div class="container d-flex">
            <div class="slide d-flex justify-content-center align-items-center">
                <img src="../images/client-logos-1.png" alt="">
            </div>
            <div class="slide d-flex justify-content-center align-items-center">
                <img src="../images/client-logos-2.png" alt="">
            </div>
            <div class="slide d-flex justify-content-center align-items-center">
                <img src="../images/client-logos-3.png" alt="">
            </div>
            <div class="slide d-flex justify-content-center align-items-center" :class="{'order' : ordine}">
                <img src="../images/client-logos-4.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppSlider',
        data(){
            return{
                ordine: false,
            }
        },
        methods: {
            greetings() {
                this.ordine = true
            },
            order2(){
                this.ordine = !this.ordine
            }
        },
        mounted() { 
            setInterval(this.greetings, 2000);
            setInterval(this.order2, 4000)
        }
    }
</script>

<style lang="scss" scoped>
    .slider{
        width: 100%;
        height: 250px;
        background-image: url(../images/rgb-gradient-bar-for-logo-carrasel.jpg);
        background-size: cover;
        overflow: hidden;
    }

    .slide{
        min-width:calc(100% / 3);
    }

    .order{
        order: -3;
    }
</style>