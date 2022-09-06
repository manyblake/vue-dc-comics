<template>
  <footer>
    <div class="footer__bg">
      <div class="container">
        <ul class="footer__list">
          <div>
            <li class="footer__links">
              <h3>Dc Comics</h3>
              <a href="#">Characters</a>
              <a href="#">Comics</a>
              <a href="#">Movies</a>
              <a href="#">TV</a>
              <a href="#">Games</a>
              <a href="#">Videos</a>
              <a href="#">News</a>
            </li>

            <li class="footer__links">
              <h3>Shop</h3>
              <a href="#">Shop DC</a>
              <a href="#">Shop DC Collectibles</a>
            </li>
          </div>

          <li class="footer__links">
            <h3>Dc</h3>
            <a href="#">Terms Of Use</a>
            <a href="#">Privacy Policy (New)</a>
            <a href="#">Ad Choice</a>
            <a href="#">Advertising</a>
            <a href="#">Jobs</a>
            <a href="#">Subscriptions</a>
            <a href="#">Talent Workshops</a>
            <a href="#">CPSC Certificates</a>
            <a href="#">Ratings</a>
            <a href="#">Shop Help</a>
            <a href="#">Contact Us</a>
          </li>

          <li class="footer__links">
            <h3>Sites</h3>
            <a href="#">DC</a>
            <a href="#">MAD Magazines</a>
            <a href="#">DC Kids</a>
            <a href="#">DC Universe</a>
            <a href="#">DC Power Visa</a>
          </li>
        </ul>

        <picture>
          <img src="@/assets/img/dc-logo-bg.png" alt="DC Logo BG" />
        </picture>
      </div>
    </div>

    <div class="footer__socials">
      <div class="container">
        <button>Sign-Up Now!</button>

        <div class="footer__links">
          <div class="footer__follow-us">
            <p>Follow Us</p>
            <a href="#">
              <img src="@/assets/img/footer-facebook.png" />
            </a>
            <a href="#">
              <img src="@/assets/img/footer-twitter.png" />
            </a>
            <a href="#">
              <img src="@/assets/img/footer-youtube.png" />
            </a>
            <a href="#">
              <img src="@/assets/img/footer-pinterest.png" />
            </a>
            <a href="#">
              <img src="@/assets/img/footer-periscope.png" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/components/variables.scss";
footer {
  color: white;

  .footer__bg {
    background-image: url(@/assets/img/footer-bg.jpg);

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
