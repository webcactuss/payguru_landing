<script setup lang="ts">
import { ref } from "vue";

import LogoWithBrads from "@/assets/img/logo-with-brands.png"
import Check from "@/assets/img/icons/Check.svg";
import Container from "@/components/Container.vue";
import Button from "@/components/Button.vue";

const items = ref([
  {
    title: "Брендирование",
    text: "Полноценный старт под вашим брендом до 7 дней: домен, логотип и первичная конфигурация."
  },
  {
    title: "Настроенные бизнес-процессы",
    text: "Готовые операционные сценарии, регламенты для поддержки, алертов и онбординга."
  },
  {
    title: "Поддержка запуска",
    text: "Учебная документация, AI White Label Kit, Trello-доски, чек-листы и пошаговые инструкции."
  },
])

</script>

<template>
  <section class="first-start">
    <Container>
      <div class="first-start__content">
        <div class="first-start__left">
          <h2>Быстрый запуск</h2>
          <div class="first-start__list">
            <div class="first-start__list-item" v-for="item in items">
              <img class="first-start__list-item-check" :src="Check" />
              <div>
                <div class="first-start__list-item-title">
                  {{ item.title }}
                </div>
                <div class="first-start__list-item-text">
                  {{ item.text }}
                </div>
              </div>
            </div>
            <Button class="first-start__action" variant="secondary">
              Запросить доступ к демо >
            </Button>
          </div>
        </div>
        <div class="first-start__right">
          <img alt="picture" :src="LogoWithBrads" />
        </div>
      </div>
    </Container>
  </section>
</template>

<style scoped lang="scss">
.first-start {
  padding: 100px 0;
  background: #020617;
  color: #fff;

  &__content {
    display: flex;
  }

  &__list {
    margin-top: 40px;
    display: flex;
    flex-direction: column;
    gap: 40px;

    &-item {
      display: flex;
      gap: 7.5px;

      &-check {
        width: 22.5px;
        height: 22.5px;
      }
      &-title {
        font-size: 21px;
        line-height: 22.5px;
      }
      &-text {
        margin-top: 10px;
        font-size: 16px;
        color: #627286;
      }
    }
  }

  &__action {
    width: 261px;
    margin-left: 30px;
  }
}
</style>
