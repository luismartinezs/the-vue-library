<template>
  <p class="paragraph" :class="{ 'dropcaps': dropcaps }">{{ text }}</p>
</template>

<script setup>
const props = defineProps({
  dropcaps: {
    type: Boolean,
    default: false
  },
  text: {
    type: String,
    default: ''
  }
});
</script>

<style lang="scss" scoped>
.paragraph {
  padding-bottom: 2rem;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;

  line-height: 1.5;
  letter-spacing: 0.3px;
  word-spacing: 2px;
  &.dropcaps {
    &:first-child::first-letter {
      color: #fe5f55;
      font-weight: bold;
      font-size: 70px;
      float: left;
      line-height: 60px;
      padding-right: 8px;
      margin-top: -3px;
    }
  }
}
</style>