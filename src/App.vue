<template>
  <div id="app">
    My Progress on course from Udemy on Vue JS 2 with Firebase by The Net Ninja
    <br />
    SECTION 3, LECTURE 26: Computed Properties (Custom Search Box) <br />
    Set Blogs.vue.active = true to see data THIS SECTION IS
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
