<script>
export default {
  props: {
    imageSrc: String,
    title: String,
    text: String,
  },
  methods: {
    handleButtonClick() {
      // azione al click
    },
  },
};
</script>

<template>
  <div class="card">
    <img :src="imageSrc" alt="Immagine della Card" />
    <h3>{{ title }}</h3>
    <p>{{ text }}</p>
    <div class="button-container">
      <button @click="handleButtonClick" class="rounded-button">
        <img src="../../public/img/next.png" alt="" />
      </button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  border: 1px solid #ccc;
  padding: 30px;
  text-align: center;
  border-radius: 100px;
  background-color: #ce7c2a;
  color: white;
  max-width: calc(20% - 20px);
  cursor: pointer;

  img {
    max-width: 100%;
  }

  h3 {
    font-size: 24px;
    margin: 0;
  }

  p {
    font-size: 16px;
    text-align: center;
    line-height: 1.8;
  }

  .button-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 10px;
  }
  .rounded-button {
    width: 40px;
    height: 40px;
    background-color: #fecb02;
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .button-icon {
    width: 20px;
    height: 20px;
    margin: auto;
  }
}

.card:hover {
  background-color: #7f7045;
}
</style>
