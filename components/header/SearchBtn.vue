<script setup lang="ts">
</script>

<template>
  <div class="search">
    <NuxtLink to="/home/search" class="search_btn">
      <Icon class="search_icon" name="tabler:search" style="color: white; font-size: 1.3rem" />
    </NuxtLink>
  </div>
</template>

<style scoped lang="scss">
.search{
  display: flex;
}
.search_btn{
  display: flex;
  justify-content: center;
  border-radius: 50%;
  background-color: transparent;
  align-self: center;
  align-items: center;
  width: 40px;
  height: 40px;
}

.search_btn:hover{
  background-color: #8c66ff;
}
</style>
