<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <main>

    <!-- SECTION-1 -->
    <section>
      <div class="container d-flex justify-content-center flex-column">
        <h1>
          Welcome to <br />
          DogMilo Pets
        </h1>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. <br />
          Ad repellendus soluta facilis.
        </p>
        <div class="d-flex">
          <button class="btn btn-custom">Get Started</button>
          <button class="custom-square-button">
            <font-awesome-icon
              :icon="['far', 'circle-play']"
              bounce
              size="lg"
            />
          </button>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
section {
  background-image: url("../../public/img/b.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 70vh;

  .container {
    height: 70vh;
    color: white;

    h1 {
      margin-bottom: 20px;
    }

    p {
      font-size: 14px;
      margin-bottom: 20px;
    }

    .btn {
      font-size: 22px;
      color: gray;
    }

    // BUTTON
    /* Stile hover dei pulsanti */
    .btn-custom {
      background-color: #cc7c2b;
      color: #fff;
      border-radius: 60px;
      font-size: 22px;
      transition: background-color 0.3s, color 0.3s, transform 0.3s;
      margin-right: 15px;
    }

    .btn-custom:hover {
      background-color: cc7c2b;
      color: #fff;
      border-radius: 60px;
      transform: scale(1.1);
    }

    .custom-square-button {
      width: 60px;
      height: 60px;
      background-color: #add8e6;
      color: #fff;
      border: none;
      border-radius: 10px;
      font-size: 22px;
      transition: background-color 0.3s, color 0.3s, transform 0.3s;
    }

    .custom-square-button:hover {
      background-color: #add8e6;
      color: #fff;
      transform: scale(1.1);
    }
  }
}
</style>
