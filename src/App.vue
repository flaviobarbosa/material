<template>
  <div id="app">
    <Sidenav />
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Sidenav from './components/Sidenav'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Sidenav
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
}
</style>
