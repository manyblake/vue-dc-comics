<template>
  <div class="main-toolbar">
    <div class="container">
      <ul class="main-toolbar__list">
        <li v-for="(widget, i) in widgets" :key="i" class="main-toolbar__item">
          <a :href="widget.link">
            <picture>
              <img :src="widget.img" />
            </picture>
            <span>{{ widget.text }}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
const widgets = [
  {
    link: "#",
    text: "Digital Comics",
    img: require("../assets/img/buy-comics-digital-comics.png"),
  },
  {
    link: "#",
    text: "DC Merchandise",
    img: require("../assets/img/buy-comics-merchandise.png"),
  },
  {
    link: "#",
    text: "Subscription",
    img: require("../assets/img/buy-comics-subscriptions.png"),
  },
  {
    link: "#",
    text: "Comic Shop Locator",
    img: require("../assets/img/buy-comics-shop-locator.png"),
  },
  {
    link: "#",
    text: "DC Power Visa",
    img: require("../assets/img/buy-dc-power-visa.svg"),
  },
];

export default {
  data() {
    return {
      widgets: widgets,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/variables.scss";
.main-toolbar {
  background-color: $dc-blue;
  color: white;
  padding: 3rem 0;

  .container {
    max-width: 1200px;
    margin: 0 auto;

    .main-toolbar__list {
      display: flex;
      justify-content: space-around;
      align-items: center;

      .main-toolbar__item {
        a {
          display: flex;
          align-items: center;
          gap: 0.5rem;

          picture {
            display: inline-block;
            width: 60px;
            height: 60px;

            img {
              height: 100%;
            }
          }
        }

        &:hover {
          transform: scale(110%);
          transition: transform 0.2s linear;
        }
      }
    }
  }
}
</style>
