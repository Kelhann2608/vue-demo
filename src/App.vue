<template>
  <div class="home">
    <img id="logo" alt="Mon logo" src="./assets/logo.png">
    <HelloWorld msg="Bienvenue sur ma chaine Youtube" />
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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;



}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: rgb(85, 230, 210);
  height: 100vh;
}

#logo {
  width: 280px;
}
</style>
