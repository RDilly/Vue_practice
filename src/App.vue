<template>
  <div id="app">
    <Header />
    <Names 
    title="list of names"
     />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Names from "./components/Names";

export default {
  name: "App",
  components: {
    Header,
    Names
  },
};
</script>

<style></style>
