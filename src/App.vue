<template>
  <div class="container-fluid">
    <b-navbar toggleable="md" type="dark" variant="dark" sticky>
      <b-container>
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
        <b-navbar-brand :to="{name:'home'}">
          <img src="@/assets/logo.png" width="30" height="30" class="d-inline-block align-top" alt="">
        </b-navbar-brand>
        <b-collapse is-nav id="nav_collapse">
            <b-navbar-nav>
              <b-nav-item :to="{name:'home'}" exact>Home</b-nav-item>
              <b-nav-item :to="{name:'about'}">About</b-nav-item>
            </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <div class="jumbotron mt-1">
      <h3>Ejemplo de Vue.js, usando Vue Router, Boostrap Vue y Vuex</h3>
      <small>
        Este es un ejemplo del uso de <b>Vue.js</b>, <b>Vue Router</b>, <b>Bootstrap Vue</b> y 
        <b>Vuex</b>.
      </small>
    </div>	
    <router-view/>
  </div>
</template>

<script>
import InvierteCadena from "@/components/InvierteCadena.vue"

export default {
   name:'app',
   components:{
     InvierteCadena
   }  
}
</script>

<style scoped>
  .jumbotron{
    background-color:navy;
    padding: 30px;
    color:white
  }

  .router-link-active{
      color:white!important
    }
</style>