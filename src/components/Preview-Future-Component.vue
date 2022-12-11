<template>
  <div
    class="modal fade"
    id="exampleModal"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">Boas Festas</h1>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <p v-if="dataChose.text">{{ dataChose.text }}</p>
          <img
            v-if="dataChose.img"
            :src="require(`..//assets/${dataChose.img}`)"
            class="img-fluid"
            alt="image future"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      randomSystemData: [
        {
          img: "img2.jpeg",
        },
        {
          text: "Desejo que este Natal seja como uma estrela brilhante, iluminando as nossas vidas e os nossos corações.",
        },
        {
          text: "Um Feliz Natal é o que desejo para você neste dia abençoado!",
        },
        {
          img: "img3.jpeg",
        },
      ],
      dataChose: {},
    };
  },
  methods: {
    handleDataChose() {
      this.dataChose =
        this.randomSystemData[
          Math.floor(Math.random() * (this.randomSystemData.length - 1)) + 1
        ];
    },
  },
  mounted() {
    this.handleDataChose();
  },
  destroyed() {
    this.handleDataChose();
  },
};
</script>

<style scoped>
.modal-dialog,
.modal-content {
  background: #2c3e50;
  color: #f3f3f3;
}
</style>