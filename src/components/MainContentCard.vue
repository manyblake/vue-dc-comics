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
  text-transform: uppercase;
  font-size: 0.75rem;
  text-align: start;
  img {
    aspect-ratio: 1/1;
    width: 100%;
    object-fit: cover;
    object-position: top;
    margin-bottom: 0.5rem;
  }

  img:hover {
    transform: scale(110%);
    transition: transform 0.2s linear;
  }
}
</style>
