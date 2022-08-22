<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">

        <pesquisar-vaga></pesquisar-vaga>

        <div class="row mt-5">
          <div class="col-6">
            <vaga></vaga>
          </div>
          <div class="col-6">
            <vaga></vaga>
          </div>
        </div>

        <div class="row mt-5">
            <div class="col-4">
                <indicador titulo="Vagas abertas" indicador="100" bg="bg-dark" color="text-light"></indicador>
            </div>

          <div class="col-4">
            <indicador titulo="Profissionais cadastrados" indicador="225" bg="bg-dark" color="text-light"></indicador>
          </div>

          <div class="col-4">
            <indicador titulo="Visitantes online" :indicador="usuariosOnline" bg="bg-white" color="text-dark"></indicador>
          </div>
        </div>
        
      </div>
    </div>
  </div>
</template>
<script>
/* eslint-disable */
import Indicador from "@/components/comuns/Indicador.vue";
import PesquisarVaga from "@/components/comuns/PesquisarVaga.vue";
import Vaga from "@/components/comuns/Vaga.vue";
export default {
  name: "Home",
  components: {
    PesquisarVaga,
    Indicador,
    Vaga,
  },
  data() {
    return {
      usuariosOnline: 0,
    }
  },
  methods: {
    getUsuariosOnline(){
      this.usuariosOnline = Math.floor(Math.random()*101) //aleatório entre 0 e 100
    },
  },
  created() {
    setInterval(this.getUsuariosOnline,1000)
  },
};
/* eslint-disable */
</script>
<style scoped>
</style>