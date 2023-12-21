<template>
  <div id="app">
    <NuevoRegalo />
    <RegalosComponente />
  </div>
</template>

<script>
import NuevoRegalo from './components/NuevoRegalo.vue';
import RegalosComponente from './components/RegalosComponente.vue';



export default {
  name: 'App',
  components: {
    RegalosComponente,
    NuevoRegalo
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
