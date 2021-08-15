<template>
  <div class="container">
    <div class="row">
      <Header />
    </div>
    <Search />
    <div class="row">
      <div class="col">
        <Profile />
      </div>
      <div class="col">
        <Repo />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Search from "./components/Search";
import Profile from "./components/Profile";
import Repo from "./components/Repo";

export default {
  name: "App",
  components: {
    Header,
    Search,
    Profile,
    Repo,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "Poppins", sans-serif;
}
</style>
