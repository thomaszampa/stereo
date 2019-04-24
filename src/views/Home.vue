<template>
  <div class="home">
    <b-container fluid class="text-container">
      <!-- STEREO -->
      <b-row>
        <b-col>
          <div class="stereo-bot">
            STEREO
            <span class="stereo-top">
              STEREO
            </span>
          </div>
        </b-col>
      </b-row>
      <!-- BY -->
      <b-row @mouseenter="enterArrow">
        <b-col>
          <div class="by">BY</div>
        </b-col>
        <!-- ARROW -->
        <transition name="fade">
          <b-col class="arrow-container" v-if="showArrow">
            <div>
              <div class="line-1"></div>
              <div class="line-2"></div>
              <div class="triangle"></div>
            </div>
          </b-col>
        </transition>
      </b-row>
      <!-- ZAMPA -->
      <b-col>
        <div class="zampa-bot">
          ZAMPA
          <span class="zampa-top">
            ZAMPA
          </span>
        </div>
      </b-col>
    </b-container>

    <!-- PLAYER -->
    <b-container fluid class="player-container">
      <b-row>
        <b-col>
          <div class="player"></div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style></style>

<script>
import Vue from "vue";
import BootstrapVue from "bootstrap-vue";

Vue.use(BootstrapVue);

import "../assets/style/vue_style.scss";
import "../assets/style/home_style.scss";

export default {
  data: function() {
    return {
      showArrow: false
    };
  },
  created: function() {},
  methods: {
    enterArrow() {
      this.showArrow = true;
    },
    exitArrow() {
      this.showArrow = false;
    }
  },
  computed: {}
};
</script>

<style></style>
