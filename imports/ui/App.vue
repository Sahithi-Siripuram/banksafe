<template>
  <div>
    <navbar/>
    <h1>Welcome to Meteor!</h1>
    <hello/>
    <info/>
  </div>
</template>

<script>
import Hello from './components/Hello.vue'
import Info from './components/Info.vue'
import Navbar from './components/Navbar.vue'
import './assets/styles.css'

export default {
  components: {
    Hello,
    Info,
    Navbar,
  },
}
</script>

<style>
  body {
    font-family: sans-serif;
    padding: 10px;
  }
</style>
