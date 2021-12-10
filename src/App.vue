
<template>
  <div class="content">
    <BackgroundWrapper :options="bgOptions">
      <RetroTitle title="RETRO" star />
      <RetroSubtitle subtitle="Cool effect" />
    </BackgroundWrapper>
    <div class="content-wrapper">
      <VParagraph
        dropcaps
        text="Drop cap or dropped capital is a large capital letter used as a decorative element at the beginning of a paragraph or section. The size of a drop cap is usually two or more lines."
      />
      <VParagraph
        text="The practice of using a large letter to mark the start of a text has been around for almost two thousand years. Illustrated caps increased usability by marking important passages and guiding readers through the text."
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import RetroTitle from "@/components/RetroTitle.vue";
import RetroSubtitle from "@/components/RetroSubtitle.vue";
import BackgroundWrapper from "@/components/BackgroundWrapper.vue";
import VParagraph from '@/components/VParagraph.vue';

const bgOptions = ref({
  type: 'retro',
  lines: true,
  grid: true
});
</script>

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
    &-wrapper {
      padding: 2rem;
    }
  }
}
</style>
