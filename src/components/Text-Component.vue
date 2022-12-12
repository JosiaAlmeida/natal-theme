<template>
  <div
    class="
      text-container
      position-fixed
      d-flex
      flex-column
      justify-content-center
      text-center text-capitalize
    "
  >
    <div class="element-container">
      <h1>Feliz Natal E um próspero 2023</h1>
      <h3>Pai Natal Tem Uma Surpresa para você</h3>
      <button
        @click="handleStateModal()"
        data-bs-toggle="modal"
        data-bs-target="#exampleModal"
        class="btn btn-primary"
      >
        Ver Surpresa
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    ["handleStateModal"]: Function,
  },
};
</script>

<style scoped>
.text-container {
  z-index: 5;
  height: 100%;
  width: 100%;
  color: #f3f3f3;
}
.element-container {
  animation: LetterAnimation 3s ease-in-out alternate infinite;
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