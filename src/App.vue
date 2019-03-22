<template>
  <div id="app">
    <link rel="stylesheet" 
        href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" 
        integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" 
        crossorigin="anonymous">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="wrapper">
      <h1 class="has-text-primary is-size-3 has-text-weight-semibold">Notee</h1>
      <div style="display:flex;">
        <div class="dashboard">
          <AsideMenu/>
        </div>
        <div style="width:100%;height:100vh;" v-if="showTaskView">
          <TasksView/>
        </div>
        <div style="width:100%;height:100vh;" v-if="showTeamSettingsView">
          <TeamView :team-members="team"></TeamView>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import AsideMenu from "./components/AsideMenu.vue";
import TasksView from "./components/TasksView.vue";
import TeamView from './components/TeamView.vue';

export default {
  name: "app",
  data() {
    return {
      showTaskView: true,
      showTeamSettingsView: false,
      team: [
        {id: 1, firstName: "Zdravko", lastName: "Gospodinov", age: 29, company: "Lindner", job:"Developer"},
        {id: 2,firstName: "Georgi", lastName: "Bonchev", age: 32, company: "Lindner", job:"Engineer"},
        {id: 3,firstName: "Gergana", lastName: "Bouklieva", age: 18, company: "Lindner", job:"Engineer"},
      ]
    };
  },
  props: {},
  components: {
    AsideMenu,
    TasksView,
    TeamView
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
  width: 350px;
  float: left;
}
</style>
