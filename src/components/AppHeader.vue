<script>
// import MyComponent from "./components/MyComponent. vue!";

export default {
  data() {
    return {
      title: "Hello world",
    };
  },

  // components: {
  //   MyComponent,
  // },
};
</script>

<template>
  <header>
    <!-- HEADER 1 -->
    <div id="header-1">
      <div class="container d-flex justify-content-between align-items-center">
        <div>
          <span> info@example.com </span>
          <span> +1(817)9013377 </span>
        </div>
        <div>
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon"/>
          <font-awesome-icon :icon="['fab', 'twitter']" class="fa-icon"/>
          <font-awesome-icon :icon="['fab', 'instagram']" class="fa-icon"/>
          <font-awesome-icon :icon="['fab', 'linkedin']" class="fa-icon"/>
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon"/>
        </div>
      </div>
    </div>
    <!-- HEADER 2 -->
    <div id="header-2">
      <div class="container"></div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  #header-1 {
    background-color: #7f7045;
    .container {
      min-height: 50px;
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
    min-height: 100px;
    background-color: blue;
  }
}
</style>
