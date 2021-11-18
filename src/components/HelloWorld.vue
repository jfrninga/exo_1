<template>
  <h1>Hello world</h1>
  <p>We have the dream big</p>
  <ul id = "exo_1">
      <li v-for = "name in names" :key="name.message">
        {{name.message}}
      </li>
  </ul>
  <div class="test"> 
    <button v-on:click = "show">appuyer pour afficher</button>
    <div v-if = "isDisplay">
      
      <button v-on:click = "hide">cacher</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data1() {
    return{
      names: [
      {message: 'SIMBARE jfr'}, 
      {message: 'GOMA esther'},
      {message: 'GOMA esther'},
      {message: 'GOMA esther'}
    ]
    }
  },
  data() {
    return {
       isDisplay: false
    };
  },
  methods: {
    show: function () {
      this.isDisplay = true;
    },
    hide: function () {
      this.isDisplay = false;
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
  /* display: inline-block; */
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
