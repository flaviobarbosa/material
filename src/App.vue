<template>
  <div id="app">
    <Sidenav />
    <router-link :to="{name: 'HelloWorld'}">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Sidenav from './components/Sidenav'
import Router from './router/index'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Sidenav,
    Router
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
