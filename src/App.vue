<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <PadreDeportes/> -->

  <!--  <PadreNumeros/> -->
 <PadreComics/>

</template>

<script>
//import PadreDeportes from './components/PadreDeportes.vue'
//import PadreNumeros from './components/PadreNumeros.vue'

import PadreComics from './components/PadreComics.vue'
export default {
  name: 'App',
  components: {
    //PadreDeportes,
    
   // PadreNumeros
    PadreComics
  }
}
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
