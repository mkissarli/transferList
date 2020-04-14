<template>
  <div>
    <h3> LIST 1 </h3>
    <ul>
      <li v-for="i in leftList" v-bind:key=i v-on:click="moveItemRight($event)">{{ i }}</li>
    </ul>
    <h3> LIST 2 </h3>
    <ul>
      <li v-for="i in rightList" v-bind:key=i v-on:click="moveItemLeft($event)">{{ i }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Transfer",
  data: () => ({
    leftList: ["1","2","3"],
    rightList: []
  }),
  computed: {
    
  },
  methods: {
    moveItemRight(e){
      var item = e.currentTarget.textContents;
      this.leftList.splice(this.leftList.indexOf(item), 1);
      this.rightList.push(item);
    },
    moveItemLeft(e){
      var item = e.currentTarget.textContents;
      this.rightList.splice(this.rightList.indexOf(item),1);
      this.leftList.push(item);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
