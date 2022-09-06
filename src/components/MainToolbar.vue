<template>
  <div class="main-toolbar">
    <div class="container">
      <ul class="main-toolbar__list">
        <li class="main-toolbar__item">
          <a href="#">
            <picture>
              <img src="@/assets/img/buy-comics-digital-comics.png" />
            </picture>
            <span>Digital Comics</span>
          </a>
        </li>
        <li class="main-toolbar__item">
          <a href="#">
            <picture>
              <img src="@/assets/img/buy-comics-merchandise.png" />
            </picture>
            <span>DC Merchandise</span>
          </a>
        </li>
        <li class="main-toolbar__item">
          <a href="#">
            <picture>
              <img src="@/assets/img/buy-comics-subscriptions.png" />
            </picture>
            <span>Subscription</span>
          </a>
        </li>
        <li class="main-toolbar__item">
          <a href="#">
            <picture>
              <img src="@/assets/img/buy-comics-shop-locator.png" />
            </picture>
            <span>Comic Shop Locator</span>
          </a>
        </li>
        <li class="main-toolbar__item">
          <a href="#">
            <picture>
              <img src="@/assets/img/buy-dc-power-visa.svg" />
            </picture>
            <span>DC Power Visa</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/components/variables.scss";
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
