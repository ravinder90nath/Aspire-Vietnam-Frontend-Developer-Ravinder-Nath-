<template>
  <div id="app">
      <sidepanel />
      <mainbody />
  </div>
</template>

<script>

import sidepanel from './components/sidenev/sidepanel.vue'
import mainbody from './components/body/mainbody.vue'

export default {
  name: 'App',
  components: {
    sidepanel,
    mainbody
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
}
</style>
