<template>
  <button @click="accionBoton({estado:estado, numero:numero})">{{textoBoton}}</button>
</template>

<script>
import { mapActions } from "vuex";
export default {
 name:'BotonAccion',
    props: {
        estado: {
            type: Boolean,
            
        },
        numero:{
            type:Number
        }   
    },
    computed: {
            textoBoton() {
                return this.estado ? 'Aumentar' : 'Disminuir' 
            }
    },
    methods: {
       ...mapActions(['accionBoton'])
    },
}
</script>

<style>

</style>