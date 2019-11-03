<template>
  <div>
    <Sidebar/>
<!--    <div class="navbar">-->
<!--      <nuxt-link to="/">Accueil</nuxt-link>-->
<!--      <nuxt-link to="/components/alert">Alertes</nuxt-link>-->
<!--      <nuxt-link to="/components/card">Cards</nuxt-link>-->
<!--      <nuxt-link to="/components/button">Button</nuxt-link>-->
<!--      <nuxt-link to="/components/elevation">Elevations</nuxt-link>-->
<!--    </div>-->
    <nuxt class="app"/>
  </div>
</template>

<script>
  import Sidebar from "../components/Sidebar";

  export default {
    name: 'layout',
    transition: 'slide-down',
    components: {Sidebar},
  }
</script>

<style lang="sass">
  @import "~/assets/scss/app.scss";
</style>
