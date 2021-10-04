<template>
  <div id="app">
    <Header :logoImage="logo" @select="genreSelect"/>
    <Albums :gnr="genre"/>
  </div>
</template>

<script>
import Header from './components/Header'
import Albums from './components/Albums.vue'

export default {
  name: 'App',
  components: {
    Header,
    Albums
  },
  data() {
    return {
      logo: 'spotify-logo.png',
      genre: ''
    }
  },
  methods: {
    genreSelect(text) {
      this.genre = text;
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/common.scss";

</style>
