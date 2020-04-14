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
    rightList: ["4"]
  }),
  computed: {
    
  },
  methods: {
    moveItemRight(e){
      console.log(e.currentTarget);
      var item = e.currentTarget.textContent;
      console.log(this.leftList);
      console.log(item);
      this.leftList.splice(this.leftList.indexOf(item), 1);
      this.rightList.push(item);
      console.log(this.rightList);
    },
    moveItemLeft(e){
      var item = e.currentTarget.textContent;
      this.rightList.splice(this.rightList.indexOf(item),1);
      this.leftList.push(item);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
