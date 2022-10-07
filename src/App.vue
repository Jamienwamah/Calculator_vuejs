<template>
  <router-link to="/CalcDev"></router-link>
  <CalcDev />
</template>

<script>
import CalcDev from "./components/CalcDev.vue";

export default {
  name: "App",
  components: {
    CalcDev
  }
};
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
