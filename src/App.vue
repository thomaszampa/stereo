<template>
  <div id="app">
    <router-view />
    <div class="nav-container">
      <div class="hamburger">
        <div></div>
        <div></div>
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import BootstrapVue from "bootstrap-vue";

Vue.use(BootstrapVue);

import "./assets/style/nav_style.scss";

export default {
  name: "App"
};
</script>

<style></style>
