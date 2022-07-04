<template>
    <div id="header-container">
        <router-link to="/" id="logo-url">
            <img :src="logo" :alt="alt" id="logo">
        </router-link>
       <div class="div">
            <h3>ESCOLA TÉCNICA ESTADUAL MONTEIRO LOBATO</h3>
       </div>
            
        
    </div>
</template>

<script>
export default {
    name:"Header",
    props:["logo", "alt"]
}
</script>

<style scoped>
    #header-container{
        background-color: #2062AD;
        display:flex;
        align-content: center;
        width: 100%;
        height: 80px;
        align-items: center;
    }
    #logo-url{
        background-color:transparent;
        width:48px;
        display:inline-flex;
    }

    #logo{
        background-color:transparent;
        width:64px;
    }
    .div{
        max-width:600px;
        margin:0 auto; 
        text-align: center;
        display:inline-flex;
        background-color:transparent;
    }
    h3{
        color:#FFF;
        background-color:transparent;
    }

</style>