<template>
  <header>
    <div class="container">
      <div class="icon">
        <img src="../assets/img/dc-logo.png" alt="DC Logo" />
      </div>
      <nav class="main-nav">
        <ul class="main-nav__list">
          <li v-for="(link, i) in links" :key="i">
            <a :class="i === 0 ? 'active' : ''" :href="link.link">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
const navbarLinks = [
  {
    text: "Characters",
    link: "#",
  },
  {
    text: "Comics",
    link: "#",
  },
  {
    text: "Movies",
    link: "#",
  },
  {
    text: "TV",
    link: "#",
  },
  {
    text: "Games",
    link: "#",
  },
  {
    text: "Collectibles",
    link: "#",
  },
  {
    text: "Videos",
    link: "#",
  },
  {
    text: "Fans",
    link: "#",
  },
  {
    text: "News",
    link: "#",
  },
  {
    text: "Shop",
    link: "#",
  },
];
export default {
  data() {
    return {
      links: navbarLinks,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/variables.scss";
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
            transition: color 0.1s linear;
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
