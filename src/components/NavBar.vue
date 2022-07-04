<template>
    <div id="nav">
    <router-link to="/">Oportunidade</router-link> 
    <router-link  to="/curriculo">Meu Currículo</router-link>
  </div>
</template>

<script>
    export default{
        name:"NavBar"
    }
</script>


<style scoped>
    #nav{
        background-color: #c2c2c2;
        border-bottom: 4px solid #c1c1c1;
        padding: 15px 50px;
        display:flex;
        margin-top:40px;
    }
    #nav a{
        padding:5px;
        background:transparent;
        text-decoration:none;
        font-size:16px;
        margin-right:40px;
        color:#222;
    }
    #nav a.router-link-exact-active{
        font-weight:bold;
    }
</style>