<template>
  <div id="app">
    <h3>Switch</h3>
    <CustomSwitch/>
    <h3>Tab</h3>
    <CustomTab/>
  </div>
</template>

<script>
import CustomSwitch from "./components/Switch";
import CustomTab from "./components/Tab";

export default {
  name: "App",
  components: {
    CustomSwitch,
    CustomTab
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

/* reset css */
body {
  margin: 0;
}
</style>
