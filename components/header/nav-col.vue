<script setup lang="ts">
defineProps({
  value: String,
  link: String,
})
</script>

<template>
  <div class="nav-col-btn">
    <NuxtLink :to="link">{{ value }}</NuxtLink>
  </div>
</template>

<style scoped lang="scss">
.nav-col-btn{
  align-items: center;
  display: flex;
  padding: 10px;
  
  a{ color: #fff; }
}
</style>