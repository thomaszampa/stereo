<template>
  <div id="title">
    <div class="stereo-container">
      <h1 class="stereo-bot">
        STEREO
        <span class="stereo-top">STEREO</span>
      </h1>
    </div>
    <div class="by-container">
      <div class="by"></div>
    </div>
  </div>
</template>

<style lang="scss">
$dark: #070707;
$blue: #061d33;
$yellow: #e8c23a;
$beige: #f2edc9;
$light: #fffdf2;

@font-face {
  font-family: BigJohnNorm;
  font-style: normal;
  font-weight: normal;
  src: url(assets/fonts/BigJohnPRO-Regular.otf) format("opentype");
}

@font-face {
  font-family: BigJohnBold;
  font-style: bold;
  font-weight: bold;
  src: url(assets/fonts/BigJohnPRO-Bold.otf) format("opentype");
}

@font-face {
  font-family: BigJohnLight;
  font-style: normal;
  font-weight: light;
  src: url(assets/fonts/BigJohnPRO-Light.otf) format("opentype");
}

header {
}

body {
  font-family: BigJohnNorm;
  font-style: normal;
  font-weight: normal;
  background: $dark;

  max-width: 100%;
  overflow-x: hidden;
}

.stereo-container {
  margin: auto;
}

.stereo-bot {
  font-family: BigJohnBold;
  font-weight: bold;
  font-size: 15vw;
  letter-spacing: -0.05em;
  color: $yellow;

  margin: auto;
  position: absolute;
  left: 3%;

  -webkit-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  &:hover {
    letter-spacing: 3vw;
    left: 2.75%;
  }
}

.stereo-top {
  font-family: BigJohnBold;
  font-weight: bold;
  font-size: 15vw;
  letter-spacing: -0.05em;
  color: $light;

  margin: auto;
  position: absolute;
  left: 0;

  -webkit-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  &:hover {
    letter-spacing: 3vw;
    left: 1%;
  }
}

.by {
  font-family: BigJohnNorm;
  font-weight: normal;
  font-size: 15vw;
  letter-spacing: -0.05em;
  color: $light;

  margin: auto;
}

footer {
}
</style>
