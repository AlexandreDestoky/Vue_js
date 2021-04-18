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
