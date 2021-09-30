<template>
  <section class="container">
    <ul class="elements">
      <li v-for="(element, index) in elements" :key="index" class="element">
        <a :href="url">
          <img
            class="logo"
            :src="require(`@/assets/img/${element.imgSrc}`)"
            :width="element.width"
            :alt="element.text"
          />
          <span class="textContent">{{ element.text }}</span></a
        >
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      elements: [
        {
          text: "DIGITAL COMICS",
          imgSrc: "buy-comics-digital-comics.png",
          url: "#",
          width: "",
          selected: false,
        },
        {
          text: "DC MERCHANDISE",
          imgSrc: "buy-comics-merchandise.png",
          url: "#",
          width: "",
          selected: false,
        },
        {
          text: "SUBSCRIPTION",
          imgSrc: "buy-comics-subscriptions.png",
          url: "#",
          width: "",
          selected: false,
        },
        {
          text: "COMIC SHOP LOCATOR",
          imgSrc: "buy-comics-shop-locator.png",
          url: "#",
          width: "",
          selected: false,
        },
        {
          text: "DC POWER VISA",
          imgSrc: "buy-dc-power-visa.svg",
          url: "#",
          width: "50",
          selected: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/style/common.scss";

.container {
  height: 10rem;
  background-color: $main__blue;
  display: flex;
  justify-content: center;
  .elements {
    margin: auto;
    max-width: $global__max__width;
    width: 100%;
    display: flex;
    justify-content: space-around;
    a {
      cursor: pointer;
      display: flex;
      align-items: center;
      color: white;
      .logo {
        margin-right: .625rem;
        height: 3.125rem;
      }
    }
  }
}
</style>
