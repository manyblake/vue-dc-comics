<template>
  <div class="card">
    <img :src="img" />
    <h4>{{ title }}</h4>
  </div>
</template>

<script>
export default {
  props: {
    img: String,
    title: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  img {
    aspect-ratio: 1/1;
    width: 100%;
    object-fit: cover;
    object-position: top;
  }
}
</style>
