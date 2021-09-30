<template>
  <div class="product">
    <div class="product__image"></div>
    <p class="product__name">CIAONE</p>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.product {
  width: calc((100% / 6) - 1rem);
  margin: 1rem 0.5rem;
  // height: 300px;
  background-color: black;
  &__image {
    height: 200px;
    width: 100%;
    background-color: rebeccapurple;
  }
  &__name {
    color: white;
    padding: 1.25rem 0;
  }
}
</style>