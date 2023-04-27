<template>
    <div class="mycard d-flex flex-column align-items-center mt-5 ">
    <img :src="card.image" alt="">
        <h5 class="mt-4">{{ card.subtitle }}</h5>
        <p class="mt-4">{{ card.paragraph }}</p>
    </div>
</template>

<script>
    export default {
        name: 'AppSingleCard',
        props: ['card']
    }
</script>

<style lang="scss" scoped>
    .mycard{
        width: calc(100% / 4);
        height: 300px;
    }

    img{
        width: 70px;
        height: 70px;
    }

    .mycard:hover h5{
        color: #6dc1cd;
    }
</style>