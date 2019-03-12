<template>
  <div :class="{ 'night': nightTheme }" id="app">
    <button @click="nightTheme = !nightTheme">toggle theme</button>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="hello" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  },

  data() {
    return {
      nightTheme: false
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
}
</style>
