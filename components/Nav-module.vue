<template>
    <div>
      <b-navbar toggleable="md" class="fixed-top" type="dark" variant="dark">
        <b-navbar-toggle
          target="nav-collapse"
          @click="isNavOpen = !isNavOpen"
          :aria-expanded="isNavOpen ? 'true' : 'false'"
          ref="toggleButton"
        >
          <template v-if="isNavOpen">
            <menu-icon/>
          </template>
          <template v-else-if="!isNavOpen">
            <close-icon/>
          </template>
        </b-navbar-toggle>
  
        <b-navbar-brand href="/">Felipe Maciel</b-navbar-brand>
  
        <b-collapse
          id="nav-collapse"
          is-nav
          :visible.sync="isNavOpen"
          @shown="focusToggle"
        >
          <b-navbar-nav>
            <b-nav-item class="text-light" href="/">Início</b-nav-item>
            <nuxt-link class="text-decoration-none mt-2 nav-link-projects" to="/projects">Projetos</nuxt-link>
            <nuxt-link class="text-decoration-none mt-2 ml-2 nav-link-projects" to="/links">Links</nuxt-link>
            <b-nav-item class="text-light" href="https://felipe.ebxdesignstudio.com/blog/" target="_blank">Blog</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </template>

  <style>
  .nav-link-projects {
    color:hsla(0,0%,100%,.5);
  }

  .nav-link-projects:hover {
    color: hsla(0,0%,100%,.75);
  }
  </style>
  
  <script>
  export default {
    data() {
      return {
        isNavOpen: false,
      };
    },
    methods: {
      focusToggle() {
        this.$nextTick(() => {
          this.$refs.toggleButton.$el.focus();
        });
      },
    },
  };
  </script>
  