<template>
  <Header :logo="logo_src" :alt="app_name" />
  <NavBar/>
  <router-view/>
  <Footer/>
</template>

<script>
import Header from "./components/Header.vue"
import NavBar from "./components/NavBar.vue"
import Footer from "./components/Footer.vue"

export default{
  components:{
    NavBar,
    Header,
    Footer
  },
  data(){
    return{
      logo_src:"./img/cimol-logo.png",
      app_name:"CIMOL"
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');
  *{
    font-family: 'Inter', sans-serif;
    margin:0;
    padding:0;
    box-sizing: border-box;
    background-color: #F4F4F4;
  }

  .main-container{
    margin:50px;
    min-height:350px;

  }
  h2{
    margin-bottom:30px;
    color:#111;
    text-align:center;
  }
</style>
