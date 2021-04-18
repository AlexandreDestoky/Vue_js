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