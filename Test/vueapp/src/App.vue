<template>
  <div id="app">
    <OneComponent />
  </div>
</template>

<script>
import OneComponent from "./components/OneComponent.vue";

export default {
  name: "App",
  components: {
    OneComponent,
  },
  data: () => ({}),
  mounted() {},
};
</script>

<style>
body {
  background: #ededed;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
