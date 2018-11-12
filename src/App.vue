<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar /> <AllFriends /> <OnlineFriends />
  </div>
</template>

<script>
import Navbar_Vue from "./Navbar.vue";
import AllFriends_Vue from "./AllFriends.vue";
import OnlineFriends_Vue from "./OnlineFriends.vue";

export default {
  name: "app",
  components: {
    Navbar: Navbar_Vue,
    AllFriends: AllFriends_Vue,
    OnlineFriends: OnlineFriends_Vue
  },
  data() {
    return {
      title: "My first Vue App"
    };
  }
};
</script>

<style>
h1 {
  color: #444;
  font-weight: normal;
  text-align: center;
}
</style>
