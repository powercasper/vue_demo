<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div :key="name" v-for="name of names">
      <MyComponent :name='name'/>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import MyComponent from "./components/myComponent.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    MyComponent
  },
  data() {
    return {
      names: ["bob", "bil", "sam", "lil"]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: aquamarine;
}
</style>
