<template>
  <div>
    <h1>Padre deportes</h1>
    <h1 style="color:red" v-if="favorito">
        {{favorito}}
    </h1>
    <ul>
      <li v-for="deport in deportes" :key="deport">
        <HijoDeporte :nombredeporte="deport"
        v-on:seleccionarFavoritoParent="seleccionarFavoritoParent" />
        
      </li>
    </ul>
  </div>
</template>

<script>
import HijoDeporte from "./HijoDeporte.vue";
export default {
  name: "PadreDeportes",
  components: {
    HijoDeporte,
  },
  methods:{
        seleccionarFavoritoParent(nombre){
            this.favorito = nombre;
        }
  },
  data() {
    return {
      deportes: ["curling", "futbol", "baloncesto", "tenis", "voley"],
      favorito : null
    };
  },
};
</script>