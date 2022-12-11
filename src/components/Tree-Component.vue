<template>
  <video class="video-main" autoplay loop muted>
    <source src="../assets/christmas5.mp4" type="video/mp4" />
  </video>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.video-main {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  filter: brightness(0.6);
}
</style>