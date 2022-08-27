<template>
    <div>
        <button @click="conteudo='home'">Home</button>
        <button @click="conteudo='publicar-vaga'">Publicar Vaga</button>
        <!-- <home></home>
        <publicar-vaga></publicar-vaga> -->
        <component :is="conteudo"></component>
    </div> 
</template>
<script>
/* eslint-disable */
    import Home from '../views/Home.vue'
    import PublicarVaga from '../views/PublicarVaga.vue'

    export default {
        name:'Conteudo',
        components: {
            Home,
            PublicarVaga,
        },
        data() {
            return {
                conteudo: 'home',
            }
        },
    }
    /* eslint-disable */
</script>
<style scoped>
    
</style>