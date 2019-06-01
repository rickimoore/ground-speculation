<template>
  <div id="app">
    <Navigation v-if="this.$router.currentRoute.name !== 'home'"/>
    <router-view/>
  </div>
</template>

<script>
  import Navigation from '@/components/Navigation'
  export default {
    components: {
      Navigation
    },
    data: () => {
      return {
        route: ''
      }
    }
  }
</script>

<style>
  @import "./assets/fonts/fonts.css";
  html, body {
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  width: 100%;
}
  .page{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  p {
    font-family: 'TheSans', sans-serif;
  }
</style>
