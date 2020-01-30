<template>
  <div id="app">
    <component :is="layout">
      <router-view />
    </component>
  </div>
</template>

<script>
import AuthLayout from "./layout/AuthLayout";
import MainLayout from "./layout/MainLayout";
export default {
  computed: {
    layout() {
      return (this.$route.meta.layout || "auth") + "-layout";
    }
  },
  components: {
    AuthLayout,
    MainLayout
  }
};
</script>

<style lang="scss">
@import "~materialize-css/dist/css/materialize.min.css";
@import "assets/index.css";
</style>
