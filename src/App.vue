<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <VirtualList :data="list"></VirtualList>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import VirtualList from "./components/VirtualList.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    VirtualList
  },
  data() {
    return {
      list: []
    };
  },
  created(){
    this.listFn()
  },
  methods:{
    listFn(){
      for(let i=0;i<100;i++){
        this.list.push({id:i,value:'Item'+i})
      }
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
