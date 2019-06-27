<template>
  <div id="app">
    <NavbarFirst />
  </div>
</template>

<script>
import NavbarFirst from './components/NavbarFirst.vue'

export default {
  name: 'app',
  components: {
    NavbarFirst
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
