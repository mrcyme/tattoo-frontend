<template>
  <div id="app">
    <Tattoos/>
  </div>
</template>

<script>
import Tattoos from './components/Tattoos.vue'

export default {
  name: 'App',
  components: {
    Tattoos
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
