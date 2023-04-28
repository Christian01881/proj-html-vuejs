<template>
    <div id="footer" class="d-flex">
        <div class="footer-1 d-flex flex-column">
            <img src="../images/medical_logo_1x_dark.png" alt="">
            <p class="pt-4 cont">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolemue launti totam aperiam, eaque ipsa quae abillo. Ivente veritas et quasi architecto beatae luptatem accusantium, remaperiamsiat. Voluptatem accusest atsium doloremque laudaien. Lorem ipsum sits dolores ets unser.</p>
            <hr class="rule">
            <h5 class="text-uppercase">Learn more about us</h5>
            <div class="d-flex gap-2 pt-5">
                <div class="d-flex justify-content-center align-items-center bg-facebook">
                    <i class="fa-brands fa-facebook-f"></i>
                </div>
                <div class="d-flex justify-content-center align-items-center bg-twitter">
                    <i class="fa-brands fa-twitter"></i>
                </div>
                <div class="d-flex justify-content-center align-items-center bg-youtube">
                    <i class="fa-brands fa-youtube"></i>
                </div>
                <div class="d-flex justify-content-center align-items-center bg-insta">
                    <i class="fa-brands fa-instagram"></i>
                </div>
            </div>
            <p class="copy">© Copyright 2012 - 2020 | Avada Theme by Theme Fusion | All Rights Reserved | Powered by WordPress</p>
        </div>
        <div class="footer-2">
            <h5 class="text-uppercase">Contact information</h5>
            <hr class="blue-rule">
            <p class="mt-5 grey"><i class="fa-solid fa-location-dot pe-3 size"></i> 121 Knight Street, London United Kingdom</p>
            <p class="mt-4 grey"><i class="fa-solid fa-phone-flip pe-3 size"></i> 1.800.458.556</p>
        </div>
        <div class="footer-2">
            <h5 class="text-uppercase">Medical departments</h5>
            <hr class="blue-rule">
            <ul>
                <li v-for="link in footerLinks" class="d-flex pt-2"><span class="chevron d-flex justify-content-center align-items-center me-4"><i class="fa-solid fa-chevron-right"></i></span>{{ link }}</li>
            </ul>
            <button class="text-uppercase btn-1">view our departments</button>
        </div>
        <div class="back-up d-flex align-items-center justify-content-center fs-4">
            <a href="#header"><i class="fa-solid fa-chevron-up"></i></a>
        </div>
    </div>
</template>

<script>
import { footerLinks } from '../data/store';
    export default {
        name: 'AppFooter',
        data(){
            return{
                footerLinks,
            }
        }
    }
</script>

<style lang="scss" scoped>
    
    #footer{
        width: 100%;
        height: 80vh;
        position: relative;

        img{
            width: 300px;
        }

    }
    
    .cont{
        font-size: 13px;
        color: grey;
        line-height: 30px;
    }

    .footer-1{
        width:calc(100% / 3);
        height: 100%;
        padding: 70px 0px 0px 70px;
    }

    .footer-2{
        width:calc(100% / 3);
        height: 100%;
        padding-top: 70px;
    }

    .rule{
        width: 100%;
        height: 3px;
        background-color: grey;
        color: grey;
        margin: 0;
    }
    .bg-facebook{
        background-color: #3c5998;
        width: 40px;
        height: 40px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }
    .bg-twitter{
        background-color: #54acee;
        width: 40px;
        height: 40px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }
    .bg-insta{
        background-color: #3f729b;
        width: 40px;
        height: 40px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }

    .bg-youtube{
        background-color: #cd201f;
        width: 40px;
        height: 40px;
        color: white;
        border-radius: 3px;
        font-size: 15px;
        cursor: pointer;
    }

    .copy{
        margin-top: 100px;
        font-size: 10px !important;
    }

    .blue-rule{
        width: 40px;
        height: 3px;
        color: #3aafbf;
        background-color: #3aafbf;
    }

    .size{
        font-size: 20px;
        color: #3aafbf;
    }

    .grey{
        color: grey;
    }

    .chevron{
        background-color: #3aafbf;
        color: white;
        border-radius: 50%;
        width: 20px;
        height: 20px;
    }

    ul{
        padding: 0;
    }

    li{
        list-style: none;
    }

    .btn-1{
        text-decoration: none;
        border: 1px solid black;
        padding: 10px 20px;
        margin-top: 40px;
    }

    .back-up{
        width: 70px;
        height: 50px;
        position: absolute;
        bottom: 1px;
        right: 100px;
        color: white;
        background-color: rgba($color: #000000, $alpha: 0.6);
        border-top-left-radius: 5px ;
        border-top-right-radius: 5px;

        &:hover{
            cursor: pointer;
        }

        a{
            text-decoration: none;
            color: white;
        }
    }
</style>