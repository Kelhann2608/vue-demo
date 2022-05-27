<template>
<div class="home">
  <img id="logo" alt="Mon logo" src="./assets/logo.png">
  <HelloWorld msg="Bienvenue sur ma chaine Youtube"/>
  </div> 
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
  background: rgb(85, 230, 210);
}
#logo {
  width: 280px;
}
</style>
