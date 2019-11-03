<template>
  <div>
    <div class="navbar">
      <nuxt-link to="/">Accueil</nuxt-link>
      <nuxt-link to="/components/alert">Alertes</nuxt-link>
      <nuxt-link to="/components/elevation">Elevations</nuxt-link>
      <nuxt-link to="/components/card">Cards</nuxt-link>
    </div>
    <nuxt class="app"/>
  </div>
</template>

<script>
  export default {
    name: 'layout',
    transition: 'slide-left',
  }
</script>

<style lang="sass">
  @import "~/assets/scss/app.scss";
</style>
