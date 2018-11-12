<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar /> <AllFriends :friends="friends" />
    <OnlineFriends :friends="friends" />
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
      title: "My first Vue App",
      friends: [
        { name: "Mario", online: true },
        { name: "Luigi", online: false },
        { name: "Toad", online: true },
        { name: "Bowser", online: false }
      ]
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
