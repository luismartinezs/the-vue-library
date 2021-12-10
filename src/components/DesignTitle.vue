https://codepen.io/havardob/pen/WNQwvze

<template>
  <div class="container">
    <h1>Design</h1>
  </div>
</template>

<style lang="scss" scoped>
// Codepen spesific styling - only to center the elements in the pen preview and viewport
.container {
  width: 100%;
  height: 100%;
  font-family: "Inter", sans-serif;
  background-color: mix(#fff, #e91e63, 82%);
  display: flex;
  align-items: center;
  justify-content: center;
}
// End Codepen spesific styling

h1 {
  color: mix(#fff, #e91e63, 85%);
  font-size: calc(1em + 300%);
  font-weight: 900;
  text-shadow: -0.0075em 0.0075em 0 mix(#fff, #e91e63, 94%),
    0.005em 0.005em 0 mix(#fff, #e91e63, 60%),
    0.01em 0.01em 0 mix(#fff, #e91e63, 62%),
    0.015em 0.015em mix(#fff, #e91e63, 64%),
    0.02em 0.02em 0 mix(#fff, #e91e63, 66%),
    0.025em 0.025em 0 mix(#fff, #e91e63, 68%),
    0.03em 0.03em 0 mix(#fff, #e91e63, 70%),
    0.035em 0.035em 0 mix(#fff, #e91e63, 72%);
}
</style>