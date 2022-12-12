<template>
  <div id="app">
    <TextComponent :handleStateModal="handleStateModal" />
    <Tree />
    <PreviewFuture v-if="stateModal" />
  </div>
</template>

<script>
import Tree from "./components/Tree-Component.vue";
import TextComponent from "./components/Text-Component";
import PreviewFuture from "./components/Preview-Future-Component";
export default {
  name: "App",
  components: {
    Tree,
    TextComponent,
    PreviewFuture,
  },
  data() {
    return {
      stateModal: false,
    };
  },
  methods: {
    handleStateModal() {
      this.stateModal = !this.stateModal;
    },
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
}
</style>
