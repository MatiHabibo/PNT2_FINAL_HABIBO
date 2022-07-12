<template>
  <div id="app">
    <Formato/>
  </div>
</template>

<script>
import Formato from './components/Formato.vue'

export default {
  name: 'App',
  components: {
    Formato
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
  margin-top: 60px;
}
</style>
