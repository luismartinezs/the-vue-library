<template>
  <h2 class="subtitle">{{ subtitle }}</h2>
</template>

<script setup>
const props = defineProps({
  subtitle: { type: String, default: 'Cool effect' }
});
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Mr+Dafoe&display=swap");

.subtitle {
  $color: #fe05e1;
  font-family: "Mr Dafoe";
  margin: 0;
  font-size: 5.5em;
  margin-top: -0.6em;
  color: white;
  text-shadow: 0 0 0.05em #fff, 0 0 0.2em $color, 0 0 0.3em $color;
  transform: rotate(-7deg);
}
</style>