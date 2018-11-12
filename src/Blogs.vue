<template>
  <div class="blogs">
    <h2>{{ blogTitle }}</h2>
    <hr />
    <button @click="changeTitle">Change Title</button>
  </div>
</template>

<script>
export default {
  name: "Blogs",
  data() {
    return {
      blogTitle: "Blogs"
    };
  },
  methods: {
    changeTitle() {
      this.blogTitle = "Amazing Blog Title";
    }
  },
  // Lifecycle hooks
  beforeCreate() {
    //alert("beforeCreate hook");
  },
  created() {
    //alert("created hook");
  },
  beforeUpdate() {
    alert("beforeUpdate hook");
  }
};
</script>

<style>
button {
  font-size: 16px;
  color: blue;
}
</style>
