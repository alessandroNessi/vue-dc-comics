<template>
  <div class="container">
    <ul class="elements">
      <!-- src="../assets/img/buy-comics-digital-comics.png" -->
      <li v-for="(element, index) in elements" :key="index" class="element"><a :href="url">
        <img class="logo" :src="'./img/'+element.imgSrc+element.imgType" :width="element.width" :alt="element.text">
        <span class="textContent">{{element.text}}</span></a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data(){
      return {
        // optionSelected: false,
        elements: [
          {
            text: "DIGITAL COMICS",
            imgSrc:"buy-comics-digital-comics",
            imgType:".png",
            url: "#",
            width: "",
            selected: false
          },
          {
            text: "DC MERCHANDISE",
            imgSrc:"buy-comics-merchandise",
            imgType:".png",
            url: "#",
            width: "",
            selected: false
          },
          {
            text: "SUBSCRIPTION",
            imgSrc:"buy-comics-subscriptions",
            imgType:".png",
            url: "#",
            width: "",
            selected: false
          },
          {
            text: "COMIC SHOP LOCATOR",
            imgSrc:"buy-comics-shop-locator",
            imgType:".png",
            url: "#",
            width: "",
            selected: false
          },
          {
            text: "DC POWER VISA",
            imgSrc:"buy-dc-power-visa",
            imgType:".svg",
            url: "#",
            width: "50",
            selected: false
          }
        ]
    }
  }
};
</script>

<style scoped lang="scss">
  @import "../assets/style/common.scss";

  .container{
    padding: 30px;
    background-color: $main__blue;
    display: flex;
    justify-content: center;
    .elements{
      margin: auto;
      max-width: $global__max__width;
      width: 100%;
      display: flex;
      justify-content: space-between;
      a{
        cursor: pointer;
        display: flex;
        align-items: center;
        color: white;
        .logo{
          margin-right: 10px;
          height: 50px;
        }
      }
    }
  }
</style>
