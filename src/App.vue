<template>
  <div id="app">
    <h1>Vue Player</h1>
    <VuePlayer />
  </div>
</template>

<script>
import VuePlayer from "./components/VuePlayer.vue";

export default {
  name: "App",
  components: {
    VuePlayer
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
