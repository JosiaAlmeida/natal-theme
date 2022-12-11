<template>
  <div class="text-container">
    <h1>Feliz Natal E um prospero 2023</h1>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.text-container {
  text-align: center;
  position: fixed;
  z-index: 5;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
h1 {
  color: #f3f3f3;
  text-transform: capitalize;
  animation: LetterAnimation 3s ease-in-out alternate infinite;
  /* animation-fill-mode: forwards; */
}

@keyframes LetterAnimation {
  from {
    transform: translateY(100px);
  }
  to {
    transform: translateX(0);
  }
}
</style>