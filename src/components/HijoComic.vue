<template>
    <div>
        
        <h1 style="color:blue">{{comic.titulo}} </h1>
        <h3>{{comic.descripcion}}</h3>
        <h3 :class="{
            rojo: comic.year <= 2000,
            verde: comic.year > 2000
            }">
            {{comic.year}}
        </h3>
        <img :src="comic.imagen" :title="comic.titulo"/>
        <br/>
        <button @click="seleccionarFavorito()">
            Seleccionar Favorito
        </button>
        <br/>
        <button @click="eliminarComic()">
            Eliminar Comic
        </button>
        
    </div>
</template>

<script>
    export default {
        name:"HijoComic",
        props:["comic","index"],
        methods:{

            eliminarComic(){
                this.$emit("eliminarComic", this.index);

            },

            seleccionarFavorito(){
                //METODO PARA LLAMAR AL PADRE Y ENVIAR NUESTRO COMIC
                this.$emit("seleccionarFavorito",this.comic);
            }
        }
    }
</script>

<style scoped>
    @import "/./src/assets/css/estilocomic.css";
</style>