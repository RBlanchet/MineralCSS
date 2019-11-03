<template>
  <nav class="sidebar">
    <div class="sidebar__logo">
      <img src="~/static/mineral.svg" alt="Logo de l'entreprise"/> <span>Mineral CSS</span>
    </div>
    <div class="sidebar__group">
      <nuxt-link to="/" class="sidebar__item">
        <i class="material-icons">home</i>
        Accueil
        {{ route }}
      </nuxt-link>
      <div class="sidebar__toggle active">
        <a @click.native="toggle(1)" event="disabled" class="sidebar__item toggle" :class="{'active' : toggleMenu[1]}">
          <i class="material-icons">web</i>
          Composants
        </a>
        <div class="sidebar__toggle--content active force">
          <nuxt-link to="/components/alert" class="sidebar__item">
            <i class="material-icons">error</i>
            Alertes
          </nuxt-link>
          <nuxt-link to="/components/button" class="sidebar__item">
            <i class="material-icons">check</i>
            Boutons
          </nuxt-link>
          <nuxt-link to="/components/card" class="sidebar__item">
            <i class="material-icons">picture_in_picture</i>
            Cards
          </nuxt-link>
          <nuxt-link to="/components/elevation" class="sidebar__item">
            <i class="material-icons">flip_to_front</i>
            Elevations
          </nuxt-link>
        </div>
      </div>
    </div>
    <div class="sidebar__footer">
      <div class="sidebar__profile">
        <img class="sidebar__profile--image" src="~/static/profile.jpg" alt="Image de profil">
        <p class="sidebar__profile--text">Bonjour Romain !</p>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'Sidebar',
    data() {
      return {
        toggleMenu: {},
        currentRoute: null,
      }
    },
    computed: {
      routes: function() {
        return this.$router.options.routes;
      },
    },
    methods: {
      toggle(index) {
        const container = this.$refs[index][0];
        const elementToggle =  container.children[1];
        if (!this.toggleMenu[index]) {
          const height = elementToggle.scrollHeight;
          elementToggle.style.maxHeight = `${height}px`;
        } else {
          elementToggle.style.maxHeight = `0px`;
        }
        this.$set(this.toggleMenu, index, !this.toggleMenu[index]);
      }
    },
    watch: {
      $route(to) {
        this.currentRoute = to.path;
      }
    },
    beforeMount() {
      this.currentRoute = this.$router.currentRoute.path;
    }
  }
</script>
