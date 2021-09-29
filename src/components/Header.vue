<template>
  <div class="container">
    <div class="logo__container">
      <a href="" class="logo">
        <img src="../assets/img/dc-logo.png" alt="dc logo">
      </a>
    </div>
    <nav>
      <ul class="options">
        <li class="option"><a href="">CIPPA</a></li>
        <li class="option">CIPPA</li>
        <li class="option">LIPPA12345646</li>
        <li class="option">CIPPA</li>
        <li class="option">CIPPA</li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
  // variabili
  @import "../assets/style/common.scss";
  $height: 150px;
  .selected{
    border-bottom: 5px solid $main__blue;
    color: $main__blue!important;
  }
  .container{
    height: $height;
    display: flex;
    .logo__container, nav{
      width: 50%;
    }
    .logo__container{
      display: flex;
      justify-content: center;
      .logo{
        padding: 30px;
        width: $height;
        img{
          width: 100%;
        }
      }
    }
    nav{
      .options{
        height: 100%;
        display: flex;
        .option{
          a{
            font-weight: 700;
            color: inherit;
          }
          color:$main__gray;
          height: 100%;
          line-height: $height;
          margin-right: 50px;
        }
      }
    }
  } 

</style>