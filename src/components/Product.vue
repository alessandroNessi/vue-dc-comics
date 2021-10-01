<template>
  <div class="product">
    <img class="product__image" :src="data.thumb" alt="" />
    <p class="product__name">{{data.series.toUpperCase()}}</p>
  </div>
</template>

<script>
export default {
  name: "Product",
  props: ["data"],
};
// computed: {
//   text: 
//     get: function() {
//         return this.data.series.toUpperCase();
//     }
// };
</script>

<style lang="scss" scoped>
.product {
  width: calc((100% / 6) - 1rem);
  margin: 1rem 0.5rem;
  &__image {
    width: 100%;
    background-color: rebeccapurple;
  }
  &__name {
    color: white;
    padding: 1.25rem 0;
  }
}
</style>