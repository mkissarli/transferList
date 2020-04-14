<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import Transfer from "@/components/Transfer.vue";

export default {
  name: "Home",
  components: {
    Transfer
  }
};
</script>
