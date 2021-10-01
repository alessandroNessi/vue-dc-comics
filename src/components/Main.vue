<template>
  <section>
    <div class="banner">
      <div class="container">
        <h2 class="current__series">CURRENT SERIES</h2>
      </div>
    </div>
    <div class="std__bgr">
      <div class="container">
        <Product :key="index" v-for="(elm, index) in myJson" :data="elm" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Main",
  components: {
    Product,
  },
  data(){
    return{
      myJson: Json,
    }
  }
};
import Product from "./Product.vue";
import Json from "./dc-comics.json";
</script>

<style scoped lang="scss">
  @import "../assets/style/common.scss";
  .std__bgr{
    background-color: $main__gray;
    .container{
      padding: 2rem;
      display: flex;
      flex-wrap: wrap;
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
