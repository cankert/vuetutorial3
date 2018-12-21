<template>
  <div id="app">
    <h1>{{title}}</h1>
    <Navbar/>
    <Blogs/>
  </div>
</template>

<script>
import Navbar from "./Navbar";
import Blogs from "./Blogs";

export default {
  name: "app",
  components: {
    Navbar,
    Blogs
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