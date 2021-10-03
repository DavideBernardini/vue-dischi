<template>
  <div id="app">
    <Header :logoImage="logo"/>
  </div>
</template>

<script>
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Header
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
