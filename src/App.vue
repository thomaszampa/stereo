<template>
  <div id="app">
    <router-view />
    <!-- NAV HAMBURGER -->
    <div class="ham-container-A">
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
        <h1>THOMAS</h1>
        <h1>ZAMPA</h1>
      </a>
    </b-container>
  </div>
</template>

<script>
import "./assets/style/nav_style.scss";

export default {
  name: "App",
  data() {
    return {
      navOpen: false
    };
  },
  methods: {
    openNav() {
      this.navOpen = !this.navOpen;
    }
  }
};
</script>

<style></style>
