<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
import AppRectangle from "./components/AppRectangle.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppRectangle, 
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <Rectangle />
  <AppFooter />
</template>

<style lang="scss">

</style>
