<template>
  <div id="app">
    <router-view />
    <!-- NAV BAR -->
    <transition name="slide-in">
      <div v-if="changeNavbar" class="nav-bar">
        <h1 class="nav-title">STEREO</h1>
      </div>
    </transition>
    <!-- NAV HAMBURGER -->
    <div class="ham-container">
      <a href="#" class="hamburger" @click="openNav">
        <div></div>
        <div class="ham-mid"></div>
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

    <!-- CURSOR -->
    <div class="cursor"></div>
    <div class="cursor_inner"></div>

    <!-- FOOTER -->
    <b-container fluid class="footer-container">
      <a href="" class="footer-TZ" style="text-decoration: none">
        <h1>THOMAS ZAMPA</h1>
      </a>
    </b-container>
  </div>
</template>

<script>
import "./assets/style/cursor.scss";
import "./assets/style/app_style.scss";

export default {
  name: "App",
  data() {
    return {
      navOpen: false,
      changeNavbar: false
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
      if (currentScrollPosition > 920) {
        this.changeNavbar = true;
      }
      if (currentScrollPosition < 920) {
        this.changeNavbar = false;
      }
    }
  },
  mounted() {
    // Listen To Scroll
    window.addEventListener("scroll", this.onScroll);

    // Listen to Cursor Position & Follow
    const cursor = document.querySelector(".cursor");
    const cursor_inner = document.querySelector(".cursor_inner");

    document.addEventListener("mousemove", e => {
      cursor.setAttribute("style", "top: " + (e.pageY - 37.5) + "px; left: " + (e.pageX - 37.5) + "px;");

      cursor_inner.setAttribute("style", "top: " + (e.pageY - 12.5) + "px; left: " + (e.pageX - 12.5) + "px;");
    });
  },
  destroy() {
    window.removeEventLsitener("scroll", this.onScroll);
  }
};
</script>

<style></style>
