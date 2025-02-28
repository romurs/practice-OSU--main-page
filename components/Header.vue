<script setup lang="ts">
import navCol from "./header/nav-col.vue";
import "../style/main.scss";
</script>

<template>
  <header>
    <div class="container">
      <div class="nav-colgroup">
        <navCol value="Главная" link="/" />
        <navCol value="Карты" link="/beatmaps"/>
        <navCol value="Рейтинг" link="/rankings"/>
        <navCol value="Сообщества" link="/community"/>
        <navCol value="Магазин" link="/store"/>
        <navCol value="Помощь" link="/wiki"/>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header{
  width: 100%;
  background-color: var(--color-primary);
}

.container{
  max-width: 1000px;
  width: calc(100%-40px);
  margin-left: auto;
  margin-right: auto;
}
.nav-colgroup{
  display: flex;
  flex: none;
  height: 50px;
  font-size: 14px;
  font-weight: 500;
}
</style>