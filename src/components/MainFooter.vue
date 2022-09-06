<template>
  <footer>
    <div class="footer__bg">
      <div class="container">
        <ul class="footer__list">
          <div>
            <li class="footer__links">
              <h3>Dc Comics</h3>
              <a v-for="(link, i) in links1" :key="i" :href="link.link">
                {{ link.text }}
              </a>
            </li>

            <li class="footer__links">
              <h3>Shop</h3>
              <a v-for="(link, i) in links2" :key="i" :href="link.link">
                {{ link.text }}
              </a>
            </li>
          </div>

          <li class="footer__links">
            <h3>Dc</h3>
            <a v-for="(link, i) in links3" :key="i" :href="link.link">
              {{ link.text }}
            </a>
          </li>

          <li class="footer__links">
            <h3>Sites</h3>
            <a v-for="(link, i) in links4" :key="i" :href="link.link">
              {{ link.text }}
            </a>
          </li>
        </ul>

        <picture>
          <img src="../assets/img/dc-logo-bg.png" alt="DC Logo BG" />
        </picture>
      </div>
    </div>

    <div class="footer__socials">
      <div class="container">
        <button>Sign-Up Now!</button>

        <div class="footer__links">
          <div class="footer__follow-us">
            <p>Follow Us</p>
            <a v-for="(social, i) in socials" :key="i" :href="social.href">
              <img :src="social.src" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
const links1 = [
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
    text: "Videos",
    link: "#",
  },
  {
    text: "News",
    link: "#",
  },
];

const links2 = [
  {
    text: "Shop DC",
    link: "#",
  },
  {
    text: "Shop DC Collectibles",
    link: "#",
  },
];

const links3 = [
  {
    text: "Terms Of Use",
    link: "#",
  },
  {
    text: "Privacy Policy (New)",
    link: "#",
  },
  {
    text: "Ad Choice",
    link: "#",
  },
  {
    text: "Advertising",
    link: "#",
  },
  {
    text: "Jobs",
    link: "#",
  },
  {
    text: "Subscriptions",
    link: "#",
  },
  {
    text: "Talent Workshops",
    link: "#",
  },
  {
    text: "CPSC Certificates",
    link: "#",
  },
  {
    text: "Ratings",
    link: "#",
  },
  {
    text: "Shop Help",
    link: "#",
  },
  {
    text: "Contact Us",
    link: "#",
  },
];

const links4 = [
  { text: "DC", link: "#" },
  { text: "MAD Magazines", link: "#" },
  { text: "DC Kids", link: "#" },
  { text: "DC Universe", link: "#" },
  { text: "DC Power Visa", link: "#" },
];

const socials = [
  {
    href: "#",
    src: require("../assets/img/footer-facebook.png"),
  },
  {
    href: "#",
    src: require("../assets/img/footer-twitter.png"),
  },
  {
    href: "#",
    src: require("../assets/img/footer-youtube.png"),
  },
  {
    href: "#",
    src: require("../assets/img/footer-pinterest.png"),
  },
  {
    href: "#",
    src: require("../assets/img/footer-periscope.png"),
  },
];

export default {
  data() {
    return {
      links1: links1,
      links2: links2,
      links3: links3,
      links4: links4,
      socials: socials,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../components/variables.scss";
footer {
  color: white;

  .footer__bg {
    background-image: url(../assets/img/footer-bg.jpg);

    .container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      max-height: 350px;
      overflow: hidden;

      picture {
        margin-left: auto;
        aspect-ratio: 1/1;
        height: 400px;

        img {
          height: 100%;
        }
      }

      .footer__list {
        display: flex;

        .footer__links {
          display: flex;
          flex-direction: column;
          padding: 0 1.5rem;

          h3 {
            text-transform: uppercase;
            padding: 1rem 0;
          }

          a {
            color: #959595;
            font-size: 0.75rem;
            line-height: 1.7;
          }
          a:hover {
            color: white;
            transition: color 0.2s linear;
          }
        }
      }
    }
  }
  .footer__socials {
    background-color: $bg-dark-grey;
    padding: 1.5rem 0;

    .container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
    }

    button {
      border: 2px solid $dc-blue;
      background-color: transparent;
      color: white;
      text-transform: uppercase;
      padding: 0.75rem;
      font-weight: 600;
      font-size: 1.25rem;
    }

    button:hover {
      background-color: $dc-blue;
      color: $bg-dark-grey;
      transition: all 0.2s linear;
    }

    .footer__links {
      display: flex;
      margin-left: auto;

      .footer__follow-us {
        display: flex;
        align-items: center;
        gap: 1rem;

        p {
          text-transform: uppercase;
          color: $dc-blue;
          font-weight: 600;
        }

        a:hover {
          filter: brightness(0) invert(1);
          transition: filter 0.2s linear;
        }
      }
    }
  }
  &:after {
    height: 3rem;
    background-color: $bg-darker-grey;
    display: block;
    content: "";
  }
}
</style>
