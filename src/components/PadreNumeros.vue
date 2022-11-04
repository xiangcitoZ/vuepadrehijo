<template>
    <div>
        <h1>Numeros Padre</h1>
        <h1 style="color:Red" >
            La suma es: {{suma}}
        </h1>
        <button  style="background-color:red" @click="generarNumero">
            Nuevo número
        </button>
        <br/>
        <div v-for="num in numeros" :key="num">
            <HijoNumero :numero="num"
            v-on:sumarNumeros="sumarNumeros"/>

        </div>
        
    </div>

</template>
<script>
    import HijoNumero from './HijoNumero.vue'
    export default {
        name : "PadreNumeros",
        components: {
            HijoNumero
        },
        methods:{
            generarNumero(){
                var random = parseInt(Math.random() * 10)+1;
                this.numeros.push(random);
            },
            sumarNumeros(valor){
                this.suma += valor;
            }
        },
        data(){
            return{
                numeros:[33,44],
                suma:0
            }
        }
    }
</script>
