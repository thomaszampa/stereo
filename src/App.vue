<template>
  <div id="app">
    <router-view />
    <!-- NAV BAR -->
    <div class="nav-container" :class="{ 'nav-container--hidden': changeNavbar }"></div>
    <!-- NAV HAMBURGER -->
    <div class="ham-container">
      <a href="#" class="hamburger" @click="openNav">
        <div></div>
        <div></div>
        <div></div>
      </a>
    </div>
    <!-- FULL-SCREEN NAV WINDOW -->
    <transition name="fade">
      <div class="menu-container" v-if="navOpen">
        <a id="button" href="#" class="closeBtn" @click="openNav" style="text-decoration: none">
          CLOSE
        </a>
        <!-- NAV LINKS -->
        <a href="" class="nav-link-1" style="text-decoration: none">LINK</a>
        <a href="" class="nav-link-2" style="text-decoration: none">LINK</a>
        <a href="" class="nav-link-3" style="text-decoration: none">LINK</a>
        <a href="" class="nav-link-4" style="text-decoration: none">LINK</a>
      </div>
    </transition>

    <!-- FOOTER -->
    <b-container fluid class="footer-container">
      <a href="" class="footer-stereo" style="text-decoration: none">
        <h1>THOMAS ZAMPA</h1>
      </a>
    </b-container>
  </div>
</template>

<script>
import "./assets/style/app_style.scss";

export default {
  name: "App",
  data() {
    return {
      navOpen: false,
      changeNavbar: false,
      lastScrollPosition: 0
    };
  },
  methods: {
    openNav() {
      this.navOpen = !this.navOpen;
    },
    onScroll() {
      // Get the current scroll position
      const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;
      // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPosition < 900) {
        return;
      }
      // Here we determine whether we need to show or hide the navbar
      this.changeNavbar = currentScrollPosition > this.lastScrollPosition;
      // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition;
    }
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  destroy() {
    window.removeEventLsitener("scroll", this.onScroll);
  }
};
</script>

<style></style>
