<script setup>
import { ref } from 'vue'
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import RetroTitle from "@/components/RetroTitle.vue";
import RetroSubtitle from "@/components/RetroSubtitle.vue";
import BackgroundWrapper from "@/components/BackgroundWrapper.vue";

const bgOptions = ref({
  type: 'retro',
  lines: true,
  grid: true
})
</script>

<template>
  <div class="content">
    <BackgroundWrapper :options="bgOptions">
      <RetroTitle title="RETRO" star />
      <RetroSubtitle subtitle="Cool effect" />
    </BackgroundWrapper>
  </div>
</template>

<style lang="scss">
#app {
  width: 100%;
  height: 100%;
  margin: 0;
  overflow: hidden;
  margin: 1rem;
  .content {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    & > * {
      width: 30rem;
      height: 30rem;
      border: 1px solid black;
      border-radius: 1rem;
    }
  }
}
</style>
