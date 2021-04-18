<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <BtnEasy txt="C'est easy"/>
    <HelloWorld msg="C'est pas si compliqué en fait !"/>
    <BtnEasy txt="Réserver ici !"/>
    <BtnEasy :txt="texteBouton"/>


  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import BtnEasy from "./components/BtnEasy.vue"

export default {
  name: 'App',
  data() {
    return {
      texteBouton:"Réservation"
    }
  },
  components: {
    HelloWorld,
    BtnEasy
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
  margin-top: 60px;
}
</style>
