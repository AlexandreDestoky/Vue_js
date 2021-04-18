<template>
  <div class="easy">
    <h2>Cliquer ci-dessous !</h2>
    <button>{{(txt)}}</button>
    <p class="desc">Description :</p>
    <p>{{resume(article)}}</p>
  </div>
</template>

<script>
export default {
  name:"BtnEasy",
  props: {
    txt:String,
    article:String
  },
  methods: {
    reverse(mot) {
      return mot.toLowerCase().split("").reverse().join("");
    },
    resume(description) {
      if(description.length > 100) return `${description.slice(0, 100)}...`;
      return description;
    }
  }
}
</script>

<style scoped>
button {
  background: lightblue;
  padding: 5px;
  font-family: cursive;
  font-size: 1.6em;
  border:3px solid navy;
  box-shadow: 3px 3px 3px black;
}

button:hover {
  background: rgb(47, 66, 173);
  cursor: pointer;
  color:#eee;
}

.desc {
  font-size:40px;
  text-decoration: underline;
}
</style>



<!-- CONTENU DE APP.VUE AVANT PRIMITIVES ET REF-->
<!--
<template>
  <div id="app">

    <BtnEasy :txt="action[0]" :article="lasagne" />
    <hr>
    <BtnEasy :txt="action[2]" :article="pizza"/>
  </div>
</template>

<script>
import BtnEasy from "./components/BtnEasy.vue";

export default {
  name: "App",
  data() {
    return {
      action: ["Réservation", "Commande", "Annulation"],
      lasagne:"Les lasagnes sont des pâtes alimentaires en forme de larges plaques. Il s'agit également de la préparation utilisant ces mêmes pâtes et généralement faite de couches alternées de pâtes, de fromage et d'une sauce tomate avec de la viande, bien qu'il en existe au poisson, notamment au saumon, et végétariennes.",
      pizza:"J'adore les pizza !"
    };
  },
  components: {
    BtnEasy,
  },
};
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
-->