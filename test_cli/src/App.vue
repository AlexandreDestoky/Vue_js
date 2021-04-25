<template>
  <div id="app">
    <p>{{recherche}}</p>
    <!-- <Card :tabFilm="films" @changementdeTitre="changementTitre($event)"/> -->
    <Card :tabFilm="films" @setRecherche="changementTitre($event)"/>
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
      recherche : "Pas encore de recherche"
    };
  },
  methods: {
    changementTitre(nouveauTitre) {
      this.recherche = nouveauTitre;
    }
  },
  components: {
    Card
  },
};
</script>

<style>
#app {
  background: bisque;
  color:blue;
}

h2 {
  font-size: 1.3em;
  text-decoration: underline;
}
</style>
