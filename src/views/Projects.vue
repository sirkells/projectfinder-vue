<template>
  <div class="projects">
    <img alt="Vue logo" src="../assets/logo.png">
    <Projects msg="Welcome to Your Projects Page"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Projects from "@/components/Projects.vue";

export default {
  name: "project",
  components: {
    Projects
  }
};
</script>