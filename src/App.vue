<template>
  <div id="app">
    <Nav />
    <Counter />
    <Posts />
  </div>
</template>

<script>
import Nav from "./components/Nav"
import Counter from "./components/Counter"
import Posts from "./components/Posts"
export default {
  name: "App",
  components: {
    Nav,
    Counter,
    Posts,
  },
}
</script>

<style></style>
