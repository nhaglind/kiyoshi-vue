<template>
  <div id="app">
    <extra></extra>
    <intro></intro>
    <chapters></chapters>
  </div>
</template>

<script>
import extra from './components/extra'
import intro from './components/intro'
import chapters from './components/chapters'
export default {
  name: 'app',
  components: {
    extra,
    intro,
    chapters
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
