https://codepen.io/ykadosh/pen/zYNxVKr

<template>
  <h1 class="retro-title" :class="{star}">
    <span>{{title}}</span>
    <span>{{title}}</span>
  </h1>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    default: 'RETRO'
  },
  star: {
    type: Boolean,
    default: false
  }
});
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Mr+Dafoe&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Exo:wght@900&display=swap");

.retro-title {
  position: relative;
  font-family: "Exo";
  font-size: 9em;
  margin: 0;
  transform: skew(-15deg);
  letter-spacing: 0.03em;

  // Star
  &.star::after {
    content: "";
    position: absolute;
    top: -0.1em;
    right: 0.05em;
    width: 0.4em;
    height: 0.4em;
    background: radial-gradient(
        white 3%,
        rgba(white, 0.3) 15%,
        rgba(white, 0.05) 60%,
        transparent 80%
      ),
      // color center-x center-y / width height
      radial-gradient(rgba(white, 0.2) 50%, transparent 60%) 50% 50% / 5% 100%,
      radial-gradient(rgba(white, 0.2) 50%, transparent 60%) 50% 50% / 70% 5%;
    background-repeat: no-repeat;
  }

  // Underneath text layer
  span:first-child {
    display: block;
    text-shadow: 0 0 0.1em #8ba2d0, 0 0 0.2em black, 0 0 5em #165ff3;
    -webkit-text-stroke: 0.06em rgba(black, 0.5);
  }

  // Overlay text layer
  span:last-child {
    position: absolute;
    left: 0;
    top: 0;
    background-image: linear-gradient(
      #032d50 25%,
      #00a1ef 35%,
      white 50%,
      #20125f 50%,
      #8313e7 55%,
      #ff61af 75%
    );
    -webkit-text-stroke: 0.01em #94a0b9;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
}
</style>