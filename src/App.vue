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
              <b-nav-item :to="{name:'frutas'}">Frutas</b-nav-item>
            </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <div class="jumbotron">
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
export default {
   name:'app'
}
</script>

<style scoped>
  .jumbotron{
    background-color:navy;
    padding: 30px;
    color:white;
    border-radius: 0;
  }

  .router-link-active{
      color:white!important
    }
</style>