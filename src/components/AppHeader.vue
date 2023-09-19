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
      <div class="container d-flex">
        <div>
          <span> info@example.com </span>
          <span> +1(817)9013377 </span>
        </div>
        <div>
            <font-awesome-icon :icon="['fab', 'facebook']" />
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
    min-height: 50px;
    background-color: #7f7045;
  }

  #header-2 {
    min-height: 100px;
    background-color: blue;
  }
}
</style>
