<template>
  <div id="app">
    My Progress on course from Udemy on Vue JS 2 with Firebase by The Net Ninja
    <hr />
    <h1>{{ title }}</h1>
    <Navbar /> <Blogs />
  </div>
</template>

<script>
import Navbar_Vue from "./Navbar.vue";
import Blogs_Vue from "./Blogs.vue";

export default {
  name: "app",
  components: {
    Navbar: Navbar_Vue,
    Blogs: Blogs_Vue
  },
  data() {
    return {
      title: "My first Vue App"
    };
  },
  methods: {}
};
</script>

<style>
h1 {
  color: #444;
  font-weight: normal;
  text-align: center;
}
</style>
