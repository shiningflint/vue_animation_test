<template>
  <div id="app">
    <my-animation/>
  </div>
</template>

<script>
import MyAnimation from './components/MyAnimation.vue'

export default {
  name: 'app',
  components: {
    MyAnimation
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
