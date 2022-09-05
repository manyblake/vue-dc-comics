<template>
  <header>
    <div class="container">
      <div class="icon">
        <img src="@/assets/img/dc-logo.png" alt="DC Logo" />
      </div>
      <nav class="main-nav">
        <ul class="main-nav__list">
          <li>
            <a class="active" href="#">Characters</a>
          </li>
          <li>
            <a href="#">Comics</a>
          </li>
          <li>
            <a href="#">Movies</a>
          </li>
          <li>
            <a href="#">TV</a>
          </li>
          <li>
            <a href="#">Games</a>
          </li>
          <li>
            <a href="#">Collectibles</a>
          </li>
          <li>
            <a href="#">Videos</a>
          </li>
          <li>
            <a href="#">Fans</a>
          </li>
          <li>
            <a href="#">News</a>
          </li>
          <li>
            <a href="#">Shop</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/components/variables.scss";
header {
  .container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;

    .icon {
      width: 7.5rem;
      padding: 1.5rem;
    }

    .main-nav {
      margin-left: auto;

      .main-nav__list {
        display: flex;
        gap: 1.5rem;
        justify-content: space-between;
        height: 100%;

        li {
          text-transform: uppercase;
          font-size: 0.75rem;
          font-weight: 600;
          position: relative;
          height: 100%;
          display: flex;
          align-items: center;

          a:hover {
            color: $dc-blue;
          }

          a.active:after {
            position: absolute;
            display: block;
            content: "";
            width: 100%;
            height: 0.25rem;
            background-color: $dc-blue;
            bottom: 0;
          }
        }
      }
    }
  }
}
</style>
