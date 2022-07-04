<template>
    <div>
        <div id="menu">
            <router-link to="/" id="menuFechado-url">
            <img :src="menuFechado" :alt="alt" id="menuFechado">
            </router-link>
        </div>
        <div id="navPrincipal">
            <router-link to="">Professor</router-link> 
            <router-link to="">Cordenação</router-link> 
            <router-link to="">Cursos</router-link> 
            <router-link to="">Alunos</router-link> 
            <router-link to="">Oportunidade</router-link> 
            <router-link to="">Armarios</router-link> 
            <router-link to="">Contato</router-link> 
            <router-link to="">Login</router-link> 
        </div>
    </div>
</template>

<script>
export default {
    name:"NavPrincipal" ,
    props:['menuFechado','alt'] 
}
</script>

<style scoped>

</style>