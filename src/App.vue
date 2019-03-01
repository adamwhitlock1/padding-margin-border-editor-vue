<template>
  <div id="app"><Styles msg="Hello from props" /></div>
</template>

<script>
import Styles from "./components/Styles";

export default {
  name: "App",
  components: {
    Styles
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
