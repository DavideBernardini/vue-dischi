<template>
  <div id="app">
    <Header :logoImage="logo"/>
    <Albums/>
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
      logo: 'spotify-logo.png'
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/common.scss";

#app {
}
</style>
