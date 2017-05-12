<template>
  <div id="app">
    <router-link to="/">Home</router-link>
    <router-link to="/coucou">Coucou</router-link>
    <navbar></navbar>
    <a @click="reset">Reset</a>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import {Store} from '@/Store.js'

export default {
  name: 'app',
  components: {navbar: Navbar},
  methods: {
    reset: () => Store.reset()
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