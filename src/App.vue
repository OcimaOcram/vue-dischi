<template>
  <div id="app">
    <MyMusics/>
  </div>
</template>

<script>
import MyMusics from './components/MyMusics.vue'

export default {
  name: 'App',
  components: {
    MyMusics
}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
