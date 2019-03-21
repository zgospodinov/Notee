<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="wrapper">
      <h1 class="has-text-primary is-size-3 has-text-weight-semibold">Notee</h1>
      <div style="display:flex;">
        <div class="dashboard">
          <AsideMenu/>
        </div>
        <div style="width:100%;height:100vh;">
          <TasksView/>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import AsideMenu from "./components/AsideMenu.vue";
import TasksView from "./components/TasksView.vue";
export default {
  name: "app",
  components: {
    AsideMenu,
    TasksView
  }
};
</script>
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 10px;
}
.wrapper {
  /* background-color:cyan; */
  margin: 0 auto;
  width: 95%;
  height: 100%;
}
.dashboard {
  width: 25%;
  float: left;
}
</style>
