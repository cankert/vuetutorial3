<template>
  <div id="app">
    <h1>{{title}}</h1>
    <Navbar/>
  </div>
</template>

<script>
import Navbar from "./Navbar";

export default {
  name: "app",
  components: {
    Navbar
  },
  data() {
    return {
      title: "My First View App"
    };
  },
  methods: {}
};
</script>

<style>
h1 {
  color: blue;
  text-align: center;
  font-weight: normal;
}
</style>