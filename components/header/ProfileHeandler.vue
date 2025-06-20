<script setup lang="ts">
</script>

<template>
  <div class="profile-heandler" v-if="true">
    <NuxtLink to="/wiki/Twitter">
      <Icon class="twitter-icon" name="streamline-logos:twitter-logo-1-solid" style="color: white; font-size: 1.3rem;" />
    </NuxtLink>
    <NuxtLink to="">
      <Icon name="healthicons:heart" style="color: white; font-size: 1.3rem;"/>
    </NuxtLink>
    <button>
      <Icon name="cif:ru" />
    </button>
    <div class="profile_notification">
      <NuxtLink to="" >
        <Icon name="mdi:comment" style="color: white; font-size: 1.3rem;"/> 0
      </NuxtLink>
      <NuxtLink to="" >
        <Icon name="material-symbols:notifications-rounded" style="color: white; font-size: 1.3rem;"/>
        122
      </NuxtLink>

    </div>
  </div>
</template>

<style scoped lang="scss">
.profile-heandler{
  display: flex;
  flex: none;
  color:#fff
}

.profile_notification{
  border: 2px solid #fff;
    border-radius: 30px;
    display: flex;
    padding: 2px;
}

.twitter-icon svg {
  stroke-width: 1.5px; /* Увеличиваем толщину */
}
</style>