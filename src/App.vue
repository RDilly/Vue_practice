<template>
  <div id="app">
    <Header />
       <Names />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Names from "./components/Names";

export default {
  name: "App",
  components: {
    Header,
    Names,
  }}

</script>

<style></style>
