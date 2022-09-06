<template>
  <div id="app">
    <MainHeader />
    <MainContent />

    <MainFooter />
  </div>
</template>

<script>
import MainHeader from "./components/MainHeader.vue";
import MainContent from "./components/MainContent.vue";
import MainFooter from "./components/MainFooter.vue";

export default {
  name: "App",
  components: {
    MainHeader,
    MainContent,
    MainFooter,
  },
};
</script>

<style lang="scss">
@import "./components/reset.scss";
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght..400;600;700&display=swap");
</style>
