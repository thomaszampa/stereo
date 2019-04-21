<template>
  <div id="app">
    <router-view />
    <!-- NAV HAMBURGER -->
    <div class="nav-container">
      <a href="#" class="hamburger" @click="openNav">
        <div></div>
        <div></div>
        <div></div>
      </a>
    </div>
    <!-- FULL-SCREEN NAV WINDOW -->
    <transition name="fade">
      <div class="menu" v-if="navOpen">
        <div class="menu-container">
          <a id="button" href="#" class="closeBtn" @="openNav">
            <i>CLOSE</i>
          </a>
          <!-- NAV LINKS -->
          <div class="nav">
            <div class="nav-item">
              <a class="nav-link-1" href="#">LINK</a>
              <a class="nav-link-2" href="#">LINK</a>
              <a class="nav-link-3" href="#">LINK</a>
              <a class="nav-link-4" href="#">LINK</a>
            </div>
          </div>
        </div>
      </div>
    </transition>
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
