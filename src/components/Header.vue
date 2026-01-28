<script setup lang="ts">
import { ref } from "vue";
import Container from "@/components/Container.vue";
import Logo from "@/assets/img/Logo.svg"
import Button from "@/components/Button.vue";

const items = ref([
  {
    label: 'О нас',
    link: '#'
  },
  {
    label: 'API Документация',
    link: '#'
  },
  {
    label: 'Условия',
    link: '#'
  },
  {
    label: 'Контакты',
    link: '#'
  },
])
</script>

<template>
  <Container>
    <header class="header">
      <div class="header__logo">
        <img :src="Logo" alt="logo" />
        <span class="header__logo-text">PayGuru</span>
      </div>
      <div class="header__nav">
        <a class="header__nav-item" v-for="(item, i) in items" :key="i" :href="item.link">{{ item.label }}</a>
      </div>
      <Button class="header__auth-btn">Sign in</Button>
    </header>
  </Container>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  height: 80px;
  align-items: center;

  &__logo {
    display: flex;
    align-items: center;
    gap: 9px;

    &-text {
      font-weight: bold;
      font-size: 23px;
    }
  }

  &__nav {
    display: flex;
    align-items: center;
    gap: 60px;
    margin-left: 80px;
  }

  &__nav-item {
    font-size: 16px;
  }

  &__auth-btn {
    margin-left:  auto;
  }
}
</style>
