<template>
  <div class="card">
    <div v-for="(film, index) in tabFilm" :key="index" class="carte">
      <h2>{{ film.titre }}</h2>
      <p>{{ film.date }}</p>
    </div>
    <button @click="deleteLastMovie">Supprimer le dernier film</button>
    <!-- <button @click="changeTitre">Modifier le titre</button> -->
    <input type="text" v-model="search" />
    <button @click="envoiRecherche">Changer la recherche</button>
  </div>
</template>

<script>
export default {
  props: {
    tabFilm: Array,
  },
  methods: {
    deleteLastMovie() {
      this.tabFilm.pop();
    },
    envoiRecherche() {
      if (this.search != "") {
        this.$emit("setRecherche", this.search);
      } else {
        this.$emit("setRecherche", "OUPS");
      }
    },
    // changeTitre() {
    //   this.$emit("changementdeTitre","Titre changé");
    // }
  },
  data() {
    return {
      search: "",
    };
  },
};
</script>

<style scoped>
.card {
  border: 1px solid black;
  padding: 10px;
}

h2 {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

.carte {
  border: 2px solid brown;
  margin: 5px auto;
  text-align: center;
  width: 60%;
  background: lightslategray;
}

button {
  display: block;
  margin: 15px auto;
  /* width: 200px; */
  padding: 15px;
  background: darkslateblue;
  color: #eee;
  font-size: 1.2rem;
  cursor: pointer;
}
</style>
