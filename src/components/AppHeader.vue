<script>
export default {
  data() {
    return {
      elements: [
        { text: "Home" },
        { text: "About" },
        { text: "Service" },
        { text: "Training" },
        { text: "Blogs" },
        { text: "Get In Touch!" },
      ],
    };
  },
  methods: {
    handleButtonClick(element) {
      // azione al click

      // stampa in console cosa hai cliccato
      console.log("Hai il cliccato su:", element.text);
    },
  },
};
</script>

<template>
  <header>
    <!-- HEADER 1 -->
    <div id="header-1">
      <div class="container d-flex justify-content-between align-items-center">
        <div>
          <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
          <span> info@example.com </span>
          <font-awesome-icon :icon="['fas', 'phone']" class="icon" />
          <span> +1(817)9013377 </span>
        </div>
        <div>
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'twitter']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'instagram']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'linkedin']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon" />
        </div>
      </div>
    </div>
    <!-- HEADER 2 -->
    <div id="header-2">
      <div class="container d-flex justify-content-between align-items-center">
        <div>
          <img src="/img/logo.png" alt="" />
        </div>
        <div>
          <ul class="d-flex">
            <li v-for="(element, index) in elements" :key="index">
              <button
                class="btn btn-custom"
                @click="handleButtonClick(element)"
              >
                {{ element.text }}
              </button>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  #header-1 {
    background-color: #7f7045;
    .container {
      min-height: 50px;

      .icon {
        color: #cc7c2b;
      }
    }

    span {
      margin-right: 15px;
      color: white;
    }

    .fa-icon {
      height: 20px;
      color: blue;
      margin-left: 4px;
    }
  }

  #header-2 {
    background-color: white;
    .container {
      min-height: 100px;
    }

    li {
      list-style: none;
      margin-left: 40px;

      .btn {
        font-size: 22px;
        color: gray;
      }

      .btn-custom {
        background-color: transparent;
        border: none;
        color: #000;
        transition: background-color 0.3s, color 0.3s;
        border-radius: 40px;
      }

      /* Stile hover dei pulsanti */
      .btn-custom:hover {
        background-color: #cc7c2b;
        color: #fff;
        border-radius: 60px;
      }
    }
  }
}
</style>
