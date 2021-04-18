<template>
  <div class="easy">
    <h2>Cliquer ci-dessous !</h2>
    <button>{{txt}}</button>
  </div>
</template>

<script>
export default {
  name:"BtnEasy",
  props: {
    txt:String
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
}

button:hover {
  background: rgb(47, 66, 173);
  cursor: pointer;
}
</style>