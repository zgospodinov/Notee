<template>
  <div class="navigation">
    <aside class="menu">
      <p class="menu-label">General</p>
      <ul class="menu-list">
        <li>
          <a class="is-size-7" @click="showTasksView">Tasks</a>
        </li>
      </ul>
      <p class="menu-label">Administration</p>
      <ul class="menu-list">
        <li>
          <a class="is-size-7" @click="showTeamSettings">Team Settings</a>
        </li>
      </ul>
    </aside>
  </div>
</template>
<script>
export default {
  name: "AsideMenu",
  props: {},
  methods: {
    showTasksView() {
      alert("task views");
    },
    showTeamSettings() {
      alert("team view settings");
    }
  }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navigation {
  background-color: rgb(196, 196, 196);
  padding: 5px;
  width: 100%;
}
p {
  text-align: left;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
  width: 100%;
}
li {
  display: inline-block;
  margin: 0 10px;
  width: 100%;
}
a {
  text-align: left;
  color: #42b983;
  padding-left: 5px;
  margin: 0px;
  width: 100%;
  /* background-color:blanchedalmond; */
}
</style>
