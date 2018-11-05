<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Services msg="Welcome to Your Services Page"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Services from "@/components/Services.vue";

export default {
  name: "services",
  components: {
    Services
  }
};
</script>