<template>
  <div class="container">
    <div class="logo__container">
      <a href="" class="logo">
        <img src="../assets/img/dc-logo.png" alt="dc logo">
      </a>
    </div>
    <nav>
      <ul class="options">
        <!-- @click="selectOption(index)"  -->
        <!-- @click="option.selected? option.selected=false: option.selected=true" -->
        <li v-for="(option, index) in options" :key="index" class="option"><a @click="optionSelected===false ? option.selected=true : options[optionSelected].selected=false; optionSelected=index; option.selected=true" :class="{selected: option.selected}" :href="option.url">{{option.text}}</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
  export default {
    name: "Header",
    // methods(){
    //   return{
    //     selectOption(index){
    //       if(optionSelected!=false){
    //         options[optionSelected].selected=false;
    //       }
    //       optionSelected=index;
    //       options[optionSelected].selected=true;
    //     },
    //   }
    // },
    data(){
      return {
        optionSelected: false,
        options: [
          {
            text: "CHARACTERS",
            url: "#",
            selected: false
          },
          {
            text: "COMICS",
            url: "#",
            selected: false
          },
          {
            text: "MOVIES",
            url: "#",
            selected: false
          },
          {
            text: "TV",
            url: "#",
            selected: false
          },
          {
            text: "GAMES",
            url: "#",
            selected: false
          },
          {
            text: "COLLECTIBLES",
            url: "#",
            selected: false
          },
          {
            text: "VIDEOS",
            url: "#",
            selected: false
          },
          {
            text: "FANS",
            url: "#",
            selected: false
          },
          {
            text: "NEWS",
            url: "#",
            selected: false
          },
          {
            text: "SHOP",
            url: "#",
            selected: false
          },
        ]
      }
    }
  };
</script>

<style scoped lang="scss">
  // variabili
  @import "../assets/style/common.scss";
  $height: 150px;
  .selected{
    box-shadow: inset  0 -5px 0px 0px $main__blue;
    color: $main__blue!important;
  }
  .container{
    height: $height;
    display: flex;
    max-width: $global__max__width;
    margin: auto;
    .logo__container, nav{
      width: 50%;
    }
    .logo__container{
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
        justify-content: space-between;
        .option{
          a{
            font-weight: 700;
            color: inherit;
          }
          color:$main__gray;
          height: 100%;
          line-height: $height;
        }
      }
    }
  } 

</style>