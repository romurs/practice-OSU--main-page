<script setup lang="ts">
defineProps({
  isScrolled: Boolean
})
</script>

<template>
    <div class="background background_tringle" :class="{ 'hide': isScrolled }"></div>
    <div class="background background_transition" :class="{ 'show': isScrolled }"></div>
</template>

<style scoped lang="scss">
.background{
  position: absolute;
  width: 100%;
  z-index: -1;
  transition: all 0.3s ease;
}

.background_tringle {
  height: 6.2rem;
  background-image: url(/public/nav2-background-hue0.png);
  background-position: bottom;
  filter: hue-rotate(255deg) saturate(0.6);
  opacity: 1;

  &.hide {
    height: 3.2rem;
    opacity: 0;
  }
}

.background_transition {
  height: 6.25rem;
  background-color: var(--color-primary);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  opacity: 0;

  &.show {
    height: 3.2rem;
    opacity: 1;
  }
}
</style>