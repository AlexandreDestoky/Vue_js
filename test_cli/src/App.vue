<template>
  <div id="app">
    <!-- <p>salut</p> -->
    <Card :tabFilm="films"/>
    <Card :tabFilm="films"/>
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "App",
  data() {
    return {
      films: [
        { titre: "Inception", date: 2010,},
        { titre: "Rocky", date: 1980 },
        { titre: "Avatar", date: 2012 },
        { titre: "Indiana Jones", date: 1988 },
      ],
    };
  },
  components: {
    Card
  },
};
</script>

<style>
#app {
  background: bisque;
}
</style>
