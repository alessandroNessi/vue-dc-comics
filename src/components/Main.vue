<template>
  <section>
    <div class="banner">
      <div class="container">
        <h2 class="current__series">CURRENT SERIES</h2>
      </div>
    </div>
    <div class="std__bgr">
      <div class="container">
        <Product/>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Main",
  components: {
    Product,
  }

  // props: {
  //   msg: String,
  // },
};
import Product from "../components/Product.vue";
</script>

<style scoped lang="scss">
  @import "../assets/style/common.scss";
  .std__bgr{
    background-color: $main__gray;
    .container{
      padding: 2rem;
    }
  }
  .container{
      max-width: 1400px;
      margin: auto;
      height: 100%;
  }
  .banner{
    height: 32rem;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    .current__series{
      color: white;
      padding: 0.5rem 1rem;
      background-color: $main__blue;
      display: inline-block;
      position: absolute;
      bottom: 0;
      transform: translate(0, 50%);
    }
  }
</style>
