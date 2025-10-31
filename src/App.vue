<template>
  <TheNavbar />
  <TheFooter />
</template>

<script>
// @ is an alias to /src
import TheNavbar from "@/components/TheNavbar.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "HomeView",
  components: {
    TheNavbar,
    TheFooter
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
