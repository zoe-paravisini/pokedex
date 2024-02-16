<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 v-if="age>20">{{ age }}</h2>
    <h2 v-else>AAAAAH</h2>
    <a :href="url">  <!-- écrit aussi 'v-bind:href="url"'-->
      <h3>{{ name }}</h3>
    </a>
    <p>
      <ol>
        <li v-for="friend of friends" :key="friend">
        {{ friend }} </li>
      </ol>
    </p>
    <h4>{{ friends }}</h4>
    <CustomButton v-on:click="mymethod"/>
  </div>
</template>

<script>
import CustomButton from './CustomButton.vue' //(pour importer des éléments, ici un bouton, à partir d'un autre fichier.)
export default {
  name: 'HelloWorld',
  components: {
    CustomButton
  },
  props: {
    msg: String
  },
  methods: {
    mymethod() {
      this.increment_age()
      console.log("clicked")
    },
    increment_age(){
      this.age += 1
    }
  },
  data () {
    return {
      name: "Lallie",
      friends: ["Elodie", "Rozenn", "Tanguy"],
      url: "https://www.google.com",
      age: 22
    }
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
</style>
