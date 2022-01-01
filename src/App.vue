<template>
  <div id="app" class="container">
    <img class="logo" src="./assets/logo.png">
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
.container{
  max-width: 600px;
  margin: 0 auto;
}
.logo{
  display: block;
  margin: 20px auto;
  height: 75px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
