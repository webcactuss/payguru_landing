<script setup lang="ts">
import Container from "@/components/Container.vue";
import { ref } from "vue";

import Rocket from "@/assets/img/rocket.png"
import SettingsBlue from "@/assets/img/settings-blue.png"
import SettingsPurple from "@/assets/img/settings-purple.png"

const items = ref([
  {
    icon: SettingsBlue,
    title: "Готовая инфраструктура",
    text: "Брендирование под клиента: домен, логотип."
  },
  {
    icon: SettingsPurple,
    title: "Постоянные обновления",
    text: "Новый функционал и методы оплаты без остановки сервисов."
  },
  {
    icon: Rocket,
    title: "Быстрый запуск",
    text: "С возможностью кастомизации методов и бизнес-логики."
  }
])
</script>

<template>
  <section class="white-label">
    <Container>
      <div class="white-label__head">
        <h2>White Label PayGuru</h2>
        <div class="white-label__head-text">
          Готовая платёжная инфраструктура для обработки и управления <br />
          денежными потоками enterprise-уровня
        </div>
        <div class="white-label__list">
          <div v-for="item in items" class="white-label__item">
            <img :src="item.icon" />
            <div class="white-label__item-title">{{ item.title }}</div>
            <div class="white-label__item-text">{{ item.text }}</div>
          </div>
        </div>
      </div>
    </Container>
  </section>
</template>

<style scoped lang="scss">
.white-label {
  background: #020617;
  padding: 100px 0;
  color: #fff;

  &__head {
    text-align: center;
    &-text {
      margin-top: 25px;
      font-size: 24px;
      color: #FFFFFF;
      opacity: 0.75;
    }
  }

  &__list {
    display: flex;
    gap: 24px;
    margin-top: 40px;
  }
  &__item {
    width: 376px;
    border: 1px solid #FFFFFF1A;
    border-radius: 20px;
    background: #FFFFFF0D;

    &-title {
      font-size: 27px;
      font-weight: bold;
      line-height: 30px;
      margin-top: 32px;
      margin-bottom: 16px;
    }

    &-text {
      padding: 0 28px;
      color: #627286;
      font-size: 18px;
      line-height: 26px;
      margin-bottom: 51px;
    }
  }
}
</style>
