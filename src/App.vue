<template>
  <div id="app">
    <MainHeader />
    <MainContent />
    <MainToolbar />
    <MainFooter />
  </div>
</template>

<script>
import MainHeader from "@/components/MainHeader.vue";
import MainContent from "@/components/MainContent.vue";
import MainFooter from "@/components/MainFooter.vue";
import MainToolbar from "@/components/MainToolbar.vue";

export default {
  name: "App",
  components: {
    MainHeader,
    MainContent,
    MainToolbar,
    MainFooter,
  },
};
</script>

<style lang="scss">
@import "@/components/reset.scss";
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
</style>
