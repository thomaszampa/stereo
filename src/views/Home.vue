<template>
  <div class="home">
    <b-container fluid>
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
      <b-row>
        <b-col>
          <div class="by">BY</div>
        </b-col>
      </b-row>
      <!-- ZAMPA -->
      <b-row>
        <b-col>
          <div class="zampa-bot">
            ZAMPA
            <span class="zampa-top">
              ZAMPA
            </span>
          </div>
        </b-col>
      </b-row>
    </b-container>

    <!-- PLAYER -->
    <b-container>
      <b-row></b-row>
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
      message: "Welcome to Vue.js!"
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>

<style></style>
