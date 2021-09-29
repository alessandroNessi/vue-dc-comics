<template>
  <div class="container">
    <ul class="options">
      <li class="option"><a href="#"><img class="logo" src="../assets/img/buy-comics-digital-comics.png" alt=""><span>DIGITAL COMICS</span></a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data(){
      return {
        // optionSelected: false,
        options: [
          {
            text: "DIGITAL COMICS",
            imgSrc:"../assets/img/buy-comics-digital-comics.png",
            url: "#",
            selected: false
          },
          {
            text: "DC MERCHANDISE",
            imgSrc:"../assets/img/buy-comics-merchandise.png",
            url: "#",
            selected: false
          },
          {
            text: "SUBSCRIPTION",
            imgSrc:"../assets/img/buy-comics-subscriptions.png",
            url: "#",
            selected: false
          },
          {
            text: "COMIC SHOP LOCATOR",
            imgSrc:"../assets/img/buy-comics-shop-locator.png",
            url: "#",
            selected: false
          },
          {
            text: "DC POWER VISA",
            imgSrc:"../assets/img/buy-dc-power-visa.svg",
            url: "#",
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
    .options{
      display: flex;
      justify-content: center;
      align-items: center;
      .option{
        margin: 0 30px;
      }
      a{
        display: flex;
        align-items: center;
        color: white;
        .logo{
          margin-right: 10px;
          width: 50px;
        }
      }
    }
  }
</style>
