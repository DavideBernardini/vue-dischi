<template>
  <div id="app">
    <Header :logoImage="logo" :gnrList="genres" @select="genreSelect"/>
    <Albums :gnr="actualGenre" @generateGenres="generatedGenres"/>
  </div>
</template>

<script>
import Header from './components/Header';
import Albums from './components/Albums.vue';

export default {
  name: 'App',
  components: {
    Header,
    Albums
  },
  data() {
    return {
      logo: 'spotify-logo.png',
      actualGenre: '',
      genres: []
    }
  },
  methods: {
    genreSelect(text) {
      this.actualGenre = text;
    },
    generatedGenres(arr) {
      this.genres = arr;
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/common.scss";

</style>
