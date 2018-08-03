<template>
  <div id="app">
    <Coffee msg="ConnXus Coffee Cam"/>
    <Info/>
  </div>
</template>

<script>
import Coffee from './components/Coffee.vue'
import Info from './components/Info.vue'

export default {
  name: 'app',
  components: {
    Coffee,
    Info
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Lato:300|Lobster');

html, body { height: 100%; }
body {
  background: #bf9c6b;
  overflow-x: hidden;
  margin: 0;
}
h1, h2, h3, h4, h5, h6 {
  font-family: 'Lobster', cursive;
}
#app {
  font-family: 'Lato', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
}
</style>
