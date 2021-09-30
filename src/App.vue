<template>
  <div id="app">
    <body>
      <Header />
      <Main />
      <Nav />
      <Footer />
    </body>
  </div>
</template>

<script>
// app.use("/public", express.static(path.join(__dirname, 'public')));
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import Nav from "./components/Nav.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Nav,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/style/common.scss";
</style>
