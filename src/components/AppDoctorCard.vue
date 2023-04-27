<template>
    <div class="doctor-card bg-white text-start">
        <img :src="card.image" alt="">
        <div class="card-content">
            <h5 class="pt-4 text-uppercase">{{ card.name }}</h5>
            <h5>{{ card.job }}</h5>
            <p class="pt-4">{{ card.paragraph }}</p>
            <div class="d-flex gap-2 pt-3">
                <div class="d-flex justify-content-center align-items-center bg-facebook">
                    <i class="fa-brands fa-facebook-f"></i>
                </div>
                <div class="d-flex justify-content-center align-items-center bg-twitter">
                    <i class="fa-brands fa-twitter"></i>
                </div>
                <div class="d-flex justify-content-center align-items-center bg-insta">
                    <i class="fa-brands fa-instagram"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppDoctorCard',
        props:['card']
    }
</script>

<style lang="scss" scoped>
    .doctor-card{
        width: calc(100% / 5);

        &:hover{
            scale: 1.1;
            box-shadow: 10px 10px 5px grey;
        }

        img{
            width: 100%;
        }
    }

    .card-content{
        width: 80%;
        margin: 0 auto;

        h5{
            font-size: 17px;
        }

        p{
            font-size: 14px;
            color: grey;
        }
    }

    .bg-facebook{
        background-color: #3c5998;
        width: 30px;
        height: 30px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }
    .bg-twitter{
        background-color: #54acee;
        width: 30px;
        height: 30px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }
    .bg-insta{
        background-color: #3f729b;
        width: 30px;
        height: 30px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }
</style>