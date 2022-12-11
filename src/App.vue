<template>
  <div id="app">
    <TextComponent />
    <Tree />
  </div>
</template>

<script>
import Tree from "./components/Tree-Component.vue";
import TextComponent from "./components/Texto-Component";
export default {
  name: "App",
  components: {
    Tree,
    TextComponent,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  background: #2c3e50;
  /* height: 100vh;
  width: 100vw; */
}
</style>
