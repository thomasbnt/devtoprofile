<template>
  <div class="mw1200">
    <noteoss/>
    <devto/>
  </div>
</template>

<script>
import devto from "./components/devto.vue";
import noteoss from "./components/noteoss.vue";

export default {
  name: "App",
  components: {
    devto,
    noteoss
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  user-select: none;
}

.mw1200 {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
