<template>
  <div class="projects">
    
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