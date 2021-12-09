<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import RetroEffect from "@/components/RetroEffect.vue";
</script>

<template>
  <RetroEffect title="RETRO" subtitle="Text effect" />
</template>

<style lang="scss">
#app {
  width: 100%;
  height: 100%;
  margin: 0;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background: radial-gradient(rgba(#7600bf, 0.5) 0%, transparent 70%),
    linear-gradient(#0b161e 40%, #202076 70%);
  perspective: 700px;
  font-size: clamp(10px, 2vw, 20px);
}
</style>
