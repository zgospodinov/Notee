<template>
  <div class="team-view-panel is-fullwidth">
    <h2 class="panel-view-title has-text-primary is-size-5">Team settings</h2>
    <div class="container is-desktop">
      <button class="button is-primary is-small" @click="createMember">
        <span class="icon">
          <i class="fas fa-user-plus"></i>
        </span>
        <span>New member</span>
      </button>

      <table class="table is-fullwidth is-striped is-size-7 team-view-panel__table">
          <thead>
              <tr>
                  <th>id</th>
                  <th>Name</th>
                  <th>Last name</th>
                  <th>Job</th>
                  <th>Company</th>
              </tr>
          </thead>
        <tbody>
          <tr v-for="(member, index) in teamMembers" :key="index">
            <td>{{member.id}}</td>
            <td>{{member.firstName}}</td>
            <td>{{member.lastName}}</td>
            <td>{{member.job}}</td>
            <td>{{member.company}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamView",
  props: {
    teamMembers: {
      type: Array,
      required: true
    }
  },
  data() {
    return {};
  },
  methods: {
    createMember() {
      alert("creating new user");
    }
  }
};
</script>

<style scoped>
.team-view-panel {
  background-color: rgba(255, 235, 205, 0.544);
  width: 100%;
  height: 100%;
}

.panel-view-title {
  margin-bottom: 10px;
  border-bottom: 1px solid;
}

.team-view-panel__table{
    margin-top: 10px;
}
</style>
