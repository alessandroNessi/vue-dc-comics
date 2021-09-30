<template>
  <section>
    <div class="footer__banner">
      <div class="container">
        <div class="container__sub left">
          <div class="left">
            <h3>{{ dccomics.title }}</h3>
            <ul>
              <li
                v-for="(element, index) in dccomics.options"
                :key="index"
                class="footer__credits"
              >
                {{ element.text }}
              </li>
            </ul>
            <h3>{{ shop.title }}</h3>
            <ul>
              <li
                v-for="(element, index) in shop.options"
                :key="index"
                class="footer__credits"
              >
                {{ element.text }}
              </li>
            </ul>
          </div>
          <div>
            <h3>{{ dc.title }}</h3>
            <ul>
              <li
                v-for="(element, index) in dc.options"
                :key="index"
                class="footer__credits"
              >
                {{ element.text }}
              </li>
            </ul>
          </div>
          <div>
            <h3>{{ sites.title }}</h3>
            <ul>
              <li
                v-for="(element, index) in sites.options"
                :key="index"
                class="footer__credits"
              >
                {{ element.text }}
              </li>
            </ul>
          </div>
        </div>
        <div class="container__sub right">
          <img class="container__sub--logo" src="../assets/img/dc-logo-bg.png" alt="dc logo">
        </div>
      </div>
    </div>
    <div class="footer__nav">
      <div class="container">
        <div class="left">
          <a href="#"><div class="button__signUp"><h3>SIGN-UP NOW!</h3></div></a>
        </div>
        <div class="right">
          <a href="#"><h2 class="social__title">FOLLOW US</h2></a>
          <a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook"></a>
          <a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter"></a>
          <a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube"></a>
          <a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a>
          <a href="#"><img src="../assets/img/footer-periscope.png" alt="maps"></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      dccomics: {
        title: "DC COMICS",
        options: [
          {
            text: "Characters",
          },
          {
            text: "Comics",
          },
          {
            text: "Movies",
          },
          {
            text: "TV",
          },
          {
            text: "Games",
          },
          {
            text: "Videos",
          },
          {
            text: "News",
          },
        ],
      },
      dc: {
        title: "DC",
        options: [
          {
            text: "Terms Of Use",
          },
          {
            text: "Privacy policy (New)",
          },
          {
            text: "Ad Choices",
          },
          {
            text: "Advertising",
          },
          {
            text: "Jobs",
          },
          {
            text: "Subscriptions",
          },
          {
            text: "Talent Workshops",
          },
          {
            text: "CPSC Certificates",
          },
          {
            text: "Ratings",
          },
          {
            text: "Shop Help",
          },
          {
            text: "Among Us",
          },
        ],
      },
      sites: {
        title: "SITES",
        options: [
          {
            text: "DC",
          },
          {
            text: "MAD Magazine",
          },
          {
            text: "DC Kids",
          },
          {
            text: "DC Universe",
          },
          {
            text: "DC Power Visa",
          },
        ],
      },
      shop: {
        title: "SHOP",
        options: [
          {
            text: "Shop DC",
          },
          {
            text: "Shop DC Collectibles",
          },
        ],
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/style/common.scss";
h3 {
  color: white;
}
.container {
  width: $global__max__width;
  height: 100%;
  margin: auto;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
  &__sub {
    padding: 1rem;
    position: relative;
    div {
      margin-right: 2rem;
    }
    display: flex;
    h3 {
      margin: 1rem 0;
    }
    .footer__credits {
      color: rgb(121, 121, 121);
    }
    &--logo{
      position: absolute;
      width: 600px;
      transform: translate(-100%, -20%);
    }
  }
}

.footer {
  &__banner {
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url("../assets/img/footer-bg.jpg");
    height: 23.75rem;
    display: flex;
  }
  &__nav {
    background-color: $main__gray;
    height: 7.5rem;
    .container{
      align-items: center;
      .left a{
        padding: 0.75rem 1rem;
        border: 4px solid $main__blue;
        display: block;
      }
      .right{
        display: flex;
        padding-left: 1rem;
        color: $main__blue;
        a{
          margin-left: 1rem;
        }
      }
    }
  }
}
</style>
