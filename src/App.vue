<template>
  <nav-component></nav-component>
  <!-- <AppHeader></AppHeader> -->
  <simulation-board></simulation-board>
</template>

<script>
import SimulationBoard from "./components/main-board/SimulationBoard.vue";
import NavComponent from "./components/navbar/NavComponent.vue";
// import AppHeader from "./components/AppHeader.vue";
export default {
  name: "App",
  components: {
    // AppHeader,
    NavComponent,
    SimulationBoard,
  },
};
</script>

<style lang="scss">
$background-color-nav: #233142;
$secondary-color: #f95959;

body {
  background-color: $background-color-nav;
  overflow-x: hidden;

}
</style>
