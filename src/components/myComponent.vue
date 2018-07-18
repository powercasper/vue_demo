<template>
  <div class="cont">
    <h1>My name is MY COMPONENT {{name}}</h1>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  props: {
    name: String
  }
};
</script>

<style scoped>
.cont {
  border: black solid;
  background-color: beige;
}
</style>
