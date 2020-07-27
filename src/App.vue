<template>
  <div id="app">
    <h3>Switch</h3>
    <custom-switch></custom-switch>
  </div>
</template>

<script>
import CustomSwitch from "./components/Switch";

export default {
  name: "App",
  components: {
    CustomSwitch
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
