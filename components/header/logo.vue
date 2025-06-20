<script setup lang="ts">
defineProps({
  isScrolled: Boolean
})


</script>

<template>
  <div class="logo_container" :class="{'scrolled' : isScrolled}">
    <NuxtLink to="/" >
      <div class="logo logo logo_bg"></div>
      <div class="logo logo_white"></div>
    </NuxtLink>
  </div>
</template>

<style scoped lang="scss">
.logo_container{

  position: relative;
  transition: all .1s ease;

  align-items: center;
  height: 100%;
   &.scrolled{
    width: 2.8rem;
    transition: all .3s ease-in-out;
   }
   &:not(.scrolled){
    width: 4.5rem;
    transition: all .3s ease-in-out;
   }
  .logo{
    background-repeat: no-repeat;
    background-size: contain;
    height: 100%;
    width: 100%;
    position: absolute;
    background-position: center;
  }
  .logo_bg{
    background-image: url(/osu-lazer-logo-triangles.svg);
    opacity: 0;
  }
  .logo_white{
    background-image: url(/osu-lazer-logo-white.svg);
  }
}

.logo_container:hover{
  scale: 1.1;
  .logo_bg{
    opacity: 1;
  }
  transition: all .1s ease;
}
</style>