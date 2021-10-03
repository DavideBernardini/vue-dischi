<template>
    <header class="d-flex align-items-center ps-3">
        <img :src="require(`../assets/images/${logoImage}`)" alt="logo spotify green">
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: ['logoImage']
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

header {
    height: 70px;
    background-color: $secondaryColor;
    img {
        height: 45px;
    }
}
</style>