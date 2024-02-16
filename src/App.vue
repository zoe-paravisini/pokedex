<template>
  <div>
    <header>
      <img src="./assets/logo.png" alt="logo">
      <link rel="preconnect" href="https://fonts.googleapis.com">
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> 
      <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&display=swap" rel="stylesheet">    </header>
    <main>
      <PokeList/>
    </main>
  </div>
</template>

<script>
import 
  PokeList from './components/PokeList.vue'

export default {
  name: 'App',
  components: {
    PokeList
  }
}
</script>

<style>
  #app {
    font-family:JetBrains ;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background-color: lightblue;
    margin: 0;
  }
</style>

<style scoped>


  header {
    display: flex;
    justify-content: space-between;
  }

  main{
    width: 70%;
    margin: auto;
  }
  img{
    width: 30%;
    margin: auto;
    padding-bottom: 50px;

  }
</style>
