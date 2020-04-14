<template>
  <div>
    <ul>
      <li v-for="i in leftList" v-bind:key=i @click:"moveItemLeft(i)">
    </ul>
    <ul>
      <li v-for="i in rightList" v-bind:key=i @click:"moveItemLeft(i)">
    </ul>
  </div>
</template>

<script>
export default {
  name: "Transfer",
  props: {
    leftList: ["1","2","3"],
    rightList: ["4","5","6","7"]
  },
  computed: {
    
  },
  methods: {
    moveItemRight(item){
      this.leftList.remove(item);
      this.rightList.append(item);
    },
    moveItemLeft(item){
      this.rightList.remove(item);
      this.leftList.append(item);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
