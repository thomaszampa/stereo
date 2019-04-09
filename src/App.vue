<template>
  <div id="player">
    <div class="title-top">
      STEREO
      <span class="title-bot">STEREO</span>
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
  font-family: BigJohn;
  font-style: normal;
  font-weight: normal;
  background: $dark;
}

.title-top {
  font-family: BigJohnBold;
  font-weight: bold;
  font-size: 12vw;
  letter-spacing: -0.05em;
  color: $yellow;

  margin: auto;
  position: absolute;
  left: 3%;

  -webkit-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  &:hover {
    letter-spacing: 0.73em;
    left: 2%;
  }
}

.title-bot {
  font-family: BigJohnBold;
  font-weight: bold;
  font-size: 12vw;
  letter-spacing: -0.05em;
  color: $light;

  margin: auto;
  position: absolute;
  left: 0;

  -webkit-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  &:hover {
    letter-spacing: 0.73em;
    left: 1%;
  }
}

footer {
}
</style>
