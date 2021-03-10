<template>
  <div id="app">
    <h1>Spelling Test</h1>
  </div>
</template>

<script>
import data from "./data";

export default {
  data() {
    return {
      questions: data,
      activeIndex: 0,
      userInput: "",
    };
  },
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
