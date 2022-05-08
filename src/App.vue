<template>
  <div id="app">
    <header>
      <app-header />
    </header>
    <main>
      <app-jumbotron />
      <app-card />
      <app-nav-card />
    </main>
    <footer>
      <app-footer-top  />
      <app-footer-bottom  />

    </footer>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbotron from "./components/AppJumbotron.vue"
import AppCard from "./components/AppCard.vue";
import AppNavCard from "./components/AppNavCard.vue"
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbotron,
    AppCard,
    AppNavCard,
    AppFooterTop,
    AppFooterBottom
  }
}
</script>

<style lang="scss">
@import "./components/style/vars";
@import './components/style/generals';

</style>
