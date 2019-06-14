<template>
  <div id="app">
    <PokemonMap/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import PokemonMap from './components/PokemonMap.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    PokemonMap
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
