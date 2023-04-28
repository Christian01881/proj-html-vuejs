<template>
    <div id="header">
        <nav class="d-flex justify-content-between align-items-center">
            <div>
                <img class="logo" src="../images/medical_logo_1x_light.png" alt="">
            </div>
            <div class="drop">
                <ul class="d-flex align-items-center justify-content-between text-white text-uppercase">
                    <li v-for="(link,index) in headerLinks" :key="index" v-show="index < 2" class="px-3 lightblue">{{ link }}</li> 
                    <li v-for="(link,index) in headerLinks" :key="index" v-show="index === 2" class="px-3 lightblue">{{ link }}</li>
                    <li v-for="(link,index) in headerLinks" :key="index" v-show="index > 2" class="px-3 lightblue"><a class="none" href="#appointment">{{ link }}</a></li>
                </ul>
                <div class="down">
                    <ul class="list-group">
                        <li class="list-group-item list-g" v-for="link in footerLinks">{{ link }}</li>
                    </ul>
                </div>
            </div>
        </nav>
        <div class="container text-white">
            <div class="header-content">
                <h1 class="">Caring <span class="turquoise">For Life</span></h1>
                <p class="mt-4">Kind wordscan be short and easy to speak, but their echoes are truly andless. Avada Health focuses on you as if it was our own family</p>
                <button class="text-white text-uppercase"><a href="#main">Learn more</a></button>
            </div>
        </div>
    </div>
</template>

<script>
import { headerLinks } from '../data/store.js';
import { footerLinks} from '../data/store.js'
    export default {
        name: 'AppHeader',
        data(){
        return {
                headerLinks,
                footerLinks
        }
    },
}
</script>

<style lang="scss" scoped>
    #header{
        width: 100%;
        height: 100vh;
        background-image: url(../images/header-image-homepage.jpg);
        background-size: cover;

        nav{
            width: 90%;
            height: 90px;
            margin: 0 auto;
        }

        .logo{
            scale: 0.9;
        }

        ul{
            list-style: none;
        }

        .lightblue:hover{
            color: #3aafbf;
        }
        

        li:last-child{
            background-color:#3aafbf;
            padding: 10px 12px;
            border-radius: 2px;
            cursor: pointer;

            &:hover{
                background-color: #327ec7;
            }
        }

        .container{
            height: calc(100% - 90px);
        }
    }

    .turquoise{
        color: #3aafbf;
    }

    .header-content{
        width: 675px;
        height: 200px;
        padding-top: 100px;
        padding-left: 100px;

        h1{
            font-size: 50px;
        }

        p{
            font-size: 18px;
        }
    }

    button{
        background-color: #3aafbf;
        text-decoration: none;
        border: none;
        padding: 10px 40px;
        margin-top: 20px;
        border-radius: 4px;

        &:hover{
            background-color: #327ec7;
        }

        a{
            text-decoration: none;
            color: white;
        }
    }

    .none{
        text-decoration: none;
        color: white;
    }

    .down{
        width: 200px;
        height: 230px;
        color: black;
        background-color: white;
        position: absolute;
        right: 385px;
        top: 60px;
        display: none;
    }

    .drop:hover .down{
        display: block !important;
    }

    .list-g{
        background-color: white !important;
        color: black !important;

        &:hover{
            background-color: grey !important;
            color: white !important;
        }
    }

    
    
</style>