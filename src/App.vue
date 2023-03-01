<template>
  <div class="container">
    <Header />
    <Services />
    <About />
    <Tasty />
    <Contacts />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Services from "./components/Services.vue";
import About from "./components/About.vue";
import Tasty from "./components/Tasty.vue";
import Contacts from "./components/Contacts.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Services,
    About,
    Tasty,
    Contacts,
    Footer,
  },
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 100vw;
  margin: 0 auto;
}
</style>
