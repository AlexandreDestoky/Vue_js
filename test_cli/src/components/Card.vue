<template>
<div class="card">
  <div v-for="(film,index) in tabFilm" :key="index" class="carte">
    <h2>{{film.titre}}</h2>
    <p>{{film.date}}</p>
  </div>
  <button @click="deleteLastMovie">Supprimer le dernier film</button>
</div>
</template>

<script>
export default {
  props: {
    tabFilm : Array
  },
  methods: {
    deleteLastMovie() {
      this.tabFilm.pop();
    }
  },
}
</script>

<style scoped>
  .card {
    border:1px solid black;
    padding:10px;
  }

  h2 {
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  }

  .carte {
    border: 2px solid brown;
    margin:5px auto;
    text-align: center;
    width: 60%;
    background: lightslategray;
  }

  button {
    display: block;
    margin:15px auto;
    /* width: 200px; */
    padding:15px;
    background: darkslateblue;
    color:#eee;
    font-size: 1.2rem;
    cursor: pointer;

  }

</style>