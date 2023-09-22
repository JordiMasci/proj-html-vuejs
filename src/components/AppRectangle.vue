<script>
export default {
  data() {
    return {
      username: "",
    };
  },

  methods: {
    selectOption(option) {
      this.username += option;
    },
  },
};
</script>

<template>
  <div class="subscribe d-flex justify-content-around">
    <div class="subscribe-image">
      <img src="../../public/img/news.png" alt="" />
    </div>
    <div class="subscribe-content">
      <h4>Subscribe to our newsletter</h4>
      <div class="input-group mb-3">
        <input
          type="text"
          class="form-control"
          placeholder="username"
          aria-label="username"
          aria-describedby="basic-addon1"
          v-model="username"
        />
        <div class="input-group-append">
          <button
            class="btn btn-outline-secondary dropdown-toggle"
            type="button"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            @
          </button>
          <div class="dropdown-menu">
            <a
              class="dropdown-item"
              href="#"
              @click="selectOption('@gmail.com')"
              >gmail.com</a
            >
            <a
              class="dropdown-item"
              href="#"
              @click="selectOption('@outlook.com')"
              >outlook.com</a
            >
            <a class="dropdown-item" href="#" @click="selectOption('@mail.com')"
              >mail.com</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.subscribe {
  max-width: 800px;
  min-height: 250px;
  background-color: #cc7c2b;
  margin: 0 auto;
  position: relative;

  img {
    height: 315px;
    position: absolute;
    top: -65px;
    left: 2%;
  }
}

.subscribe-content {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 400px;

  button {
    background-color: white;
  }

  button:hover {
    color: black;
  }
}
</style>
