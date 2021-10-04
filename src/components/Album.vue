<template>
    <div class="album col mb-4">
        <div class="box p-5 p-sm-3">
            <img :src="info.poster" :alt="info.title">
            <h3 class="text-white pt-5 pt-sm-4">{{info.title}}</h3>
            <div class="author pt-3 pt-sm-2">{{info.author}}</div>
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
            height: 50%;
            object-fit: contain;
        }
        h3 {
            color: #fff;
            text-transform: uppercase;
            word-break: break-word;
            font-size: 1.625rem;
        }
        .author, .year {
            color: #808078;
            font-size: 1.25rem;
        }
    }
    
}
</style>