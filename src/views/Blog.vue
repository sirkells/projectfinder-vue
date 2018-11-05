<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Blog msg="Welcome to Your Blog Page"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Blog from "@/components/Blog.vue";

export default {
  name: "blog",
  components: {
    Blog
  }
};
</script>