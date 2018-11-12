// Added custom [active] flag to stop it from fetching JSON while editting in
CodeSandbox.io

<script>
export default {};
</script>

<style></style>
<template>
  <div class="blogs">
    <h2>{{ blogTitle }} - Active = ({{ active }})</h2>
    SEARCH:<input type="text" v-model="searchTerm" />
    <hr />
    <div v-for="post in filteredPosts" :key="post.id">
      <h3>{{ post.title }}</h3>

      <p>{{ post.body | snippet }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Blogs",
  data() {
    return {
      blogTitle: "Blogs",
      active: false,
      searchTerm: "",
      posts: []
    };
  },
  methods: {},
  computed: {
    filteredPosts() {
      return this.posts.filter(post => {
        return post.title.match(this.searchTerm);
      });
    }
  },
  // Lifecycle hooks
  created() {
    // get sample JSON from https://jsonplaceholder.typicode.com/
    // axios returns a promise
    if (this.active) {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then(response => {
          console.log(response);
          this.posts = response.data;
        })
        .catch(err => {
          console.log(err);
        });
    }
  }
};
</script>

<style>
button {
  font-size: 16px;
  color: blue;
}
</style>
