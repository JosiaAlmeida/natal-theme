<template>
  <div class="video-container">
    <video class="video-main" playsinline="" preload="auto" autoplay loop muted>
      <source src="..//assets/Untitled.mp4" type="video/mp4" />
    </video>
  </div>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.video-container {
  position: fixed;
  right: 0;
  bottom: 0;
  height: 100vh;
  width: 100vw;
}
.video-main {
  min-width: 100%;
  min-height: 100%;
  filter: brightness(0.6);
}
@media screen and (max-width: 920px) {
  .video-container {
    left: 0 !important;
    right: none;
    margin-left: calc(100vw - 200%);
  }
  .video-main {
  }
}
</style>