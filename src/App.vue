<template>
  <div id="app">
    <giphy query="kermittyping" apiKey="FWCVxq99r64wpHlrUp4mQ3YyCWVnUvuP"></giphy>
    <Deadline/>
    <!-- <img alt="Vue logo" src="./assets/fasttyping.gif"> -->

  </div>
</template>

<script>
import Deadline from './components/Deadline.vue'
import giphy from './components/Giphy'

export default {
  name: 'app',
  components: {
    Deadline,
    giphy
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #01c20bee;
  margin-top: 60px;
}
</style>
