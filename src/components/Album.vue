<template>
    <div class="album col-12 col-sm-6 col-md-4 col-lg-2 mb-4 mx-lg-1 px-3 px-lg-0">
        <div class="box p-5 p-sm-4">
            <img :src="info.poster" :alt="info.title">
            <h3 class="text-white pt-5 pt-sm-4">{{info.title}}</h3>
            <div class="author pt-4 pt-sm-3">{{info.author}}</div>
            <div class="year">{{info.year}}</div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'Album',
    props: ['info']
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.album {
    text-align: center;
    .box {
        background-color: $secondaryColor;
        height: 100%;
        img {
            width: 100%;
        }
        h3 {
            color: #fff;
            text-transform: uppercase;
            font-size: 26px;
        }
        .author, .year {
            color: #808078;
            font-size: 1.125rem;
        }
    }
    
}
</style>