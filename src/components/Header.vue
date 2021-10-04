<template>
    <header class="d-flex align-items-center ps-3 pe-4">
        <img :src="require(`../assets/images/${logoImage}`)" alt="logo spotify green">
            <select name="genre_select" id="genre_select" class="form-select" v-model="inputSelect" @change="$emit('select', inputSelect)">
                <option value="" selected>Select music genre</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
        </select>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: ['logoImage'],
    data() {
        return {
            inputSelect: ''
        }
    }
}

</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

header {
    height: 70px;
    background-color: $secondaryColor;
    img {
        height: 2.8125rem;
    }
    select {
    width: inherit;
    margin-left: auto;
}
}
</style>