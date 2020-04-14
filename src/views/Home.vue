<template>
<div class="home">
  <h2>Lists?</h2>
  <transfer></transfer>
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
