<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="wrapper">
      <h1>Notee</h1>
      <div class="dashboard">
        <AsideMenu/>
      </div>
    </div>
  </div>
</template>

<script>
import AsideMenu from "./components/AsideMenu.vue";
// import bulma from './node_modules/bulma/css/bulma.css.css"'

export default {
  name: "app",
  components: {
    AsideMenu
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
.wrapper{
  background-color:cyan;
  margin: 0 auto;
  width:95%;
  height:100%;  
}

.dashboard {
  width: 25%;
  float: left;
}
</style>
