<script setup lang="ts">
import navCol from "./header/nav-col.vue";
import Logo from "./header/logo.vue";
import Background from "./header/background.vue";
import SearchBtn from "./header/SearchBtn.vue";
import ProfileHeandler from "./header/ProfileHeandler.vue";
import "../style/main.scss";
import { ref, onMounted, onBeforeUnmount } from "vue";

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <header>
    <Background :isScrolled="isScrolled"/>
    <div class="container">
      <div class="nav-colgroup" :class="{ 'nav-scrolled': isScrolled }">
        <div class="nav-btns">
          <Logo :isScrolled="isScrolled" />
          <navCol value="Главная" link="/" />
          <navCol value="Карты" link="/beatmaps" />
          <navCol value="Рейтинг" link="/rankings" />
          <navCol value="Сообщества" link="/community" />
          <navCol value="Магазин" link="/store" />
          <navCol value="Помощь" link="/wiki" />
          <SearchBtn />
        </div>
        <ProfileHeandler/>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  position: fixed;
  width: 100%;
  z-index: 100;
}

.container {
  max-width: 1000px;
  width: calc(100% - 40px);
  margin-left: auto;
  margin-right: auto;
  z-index: 1;
}

.nav-btns {
  display: flex;
  flex: none;
  height: 100%;
  margin-right: auto;
}

.nav-colgroup {
  display: flex;
  align-items: center;
  font-size: 14px;
  font-weight: 500;

  &.nav-scrolled {
    height: 3.2rem;
    transition: all 0.3s ease;
  }

  &:not(.nav-scrolled) {
    height: 6.25rem;
    transition: all 0.3s ease;
  }
}
</style>
