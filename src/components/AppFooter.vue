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

        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppFooter'
    }
</script>

<style lang="scss" scoped>
    
    #footer{
        width: 100%;
        height: 80vh;

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
</style>