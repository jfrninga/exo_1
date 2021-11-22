<template>
  <h1>Hello world</h1>
  <p>We have the dream big</p>
  <ul id = "exo_1"  v-if = isDisplay>
      <li v-for = "name in names" :key="name.message">
        {{name.message}}
      </li>
  </ul>
  <div class="test"> 
    <div v-if = !isDisplay>
        <button v-on:click ="isDisplay = true">appuyer pour afficher</button>
    </div>
    <div v-if = isDisplay>
        <button v-on:click ="isDisplay = false">cacher</button>
    </div>
  </div>
</template>

<script>
var exo = document.getElementById("exo_1");
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  
  data() {
    return{
      names: [
      {message: 'Chris'}, 
      {message: 'Esther'},
      {message: 'Prince'},
      {message: 'Zali'},
      {message: 'Matt'}
    ],
    isDisplay: false
    }
  },
  
  methods: {
    show: function () {
      exo.isDisplay = true;
    },
    hide: function () {
      exo.isDisplay = false;
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
  color: white;
  background-color: rgba(14, 78, 197, 0.801);
  border-radius: 6px;
  padding: 5px;
}
</style>
