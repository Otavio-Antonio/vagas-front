<template>
    <div>
        <h1>Conteudo 1</h1>
        <home></home>
        <publicar-vaga></publicar-vaga>
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
        }
    }
    /* eslint-disable */
</script>
<style scoped>
    
</style>