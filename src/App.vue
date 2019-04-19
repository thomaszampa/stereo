<template>
  <div id="app">
    <router-view />
    <div class="nav-container">
      <a href="#" class="hamburger" @click="openNav">
        <div></div>
        <div></div>
        <div></div>
      </a>
    </div>
    <transition name="fade">
      <div class="menu" v-if="navOpen">
        <div class="menu-container">
          <a id="button" href="#" @click="openNav"> CLOSE BUTTON</a>
          <div class="nav">
            <div class="nav-item">
              <a class="nav-link" href="#">LINK</a>
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
