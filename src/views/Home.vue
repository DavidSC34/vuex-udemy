<template>
  <div class="home">
    
 
  <h1 :style="colorcontador" >Mi contador {{contador}}</h1>
  <button @click="accionIncrementar">Aumentar</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions } from "vuex";



export default {
  name: 'Home',
  components: {
    
  },
  computed:{
    ...mapState(['contador']),
    colorcontador(){
      return [this.contador > 100 ? {'color':'green'} :{'color':'red'}]
    }
  },
  methods:{
    // ...mapMutations(['incrementar']) no se recomienda
    ...mapActions(['accionIncrementar'])
  }
}
</script>
