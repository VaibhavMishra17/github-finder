<template>
  <header>
    <h1>All Repositories</h1>
  </header>
  <div class="container">
    <table class="table is-bordered is-striped is-hoverable is-fullwidth">
      <thead>
        <tr>
          <th>Name</th>
          <th>URL</th>
          <th>Language</th>
          <th>description</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="repo in repos" v-bind:key="repo.id">
          <td>{{ repo.name }}</td>
          <td>{{ repo.html_url }}</td>
          <td>{{ repo.language }}</td>
          <td>{{ repo.description }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Repo",
  data() {
    return {
      repos: null,
    };
  },
  created: function() {
    axios
      .get("https://api.github.com/users/VaibhavMishra17/repos")
      .then((response) => {
        this.repos = response.data;
      });
  },
};
</script>
