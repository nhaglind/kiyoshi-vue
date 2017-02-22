<template>
  <div id="app">
    <extra></extra>
    <test></test>
  </div>
</template>

<script>
import test from './components/test'
import extra from './components/extra'
export default {
  name: 'app',
  components: {
    test,
    extra
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
