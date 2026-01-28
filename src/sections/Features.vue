<script setup lang="ts">
import Container from "@/components/Container.vue";
import { ref } from "vue";

import FeaturesImg from "@/assets/img/featuresImg.png"
import Check from "@/assets/img/icons/whiteCheck.svg";
import Button from "@/components/Button.vue";

const items = ref([
  {
    title: "Круглосуточная поддержка 24/7",
    text: "Дежурная команда специалистов для оперативного реагирования"
  },
  {
    title: "Мониторинг",
    text: "Непрерывный контроль сервисов с автоматическими оповещениями в Telegram"
  },
  {
    title: "Полное логирование",
    text: "Детальные логи, аудит операций и прозрачная трассировка запросов"
  },
]);
</script>

<template>
  <div class="features">
    <Container>
      <div class="features__content">
        <img :src="FeaturesImg" alt="picture" />
        <div class="features__list">
          <div class="features__list-item" v-for="item in items">
            <img class="features__list-item-check" :src="Check" />
            <div>
              <div class="features__list-item-title">
                {{ item.title }}
              </div>
              <div class="features__list-item-text">
                {{ item.text }}
              </div>
            </div>
        </div>
        <Button class="features__action" variant="secondary">
          Запланировать звонок >
        </Button>
      </div>
      </div>
    </Container>
  </div>
</template>

<style scoped lang="scss">
.features {
  padding: 100px 0;
  background: #564CF1;
  color: #fff;

  &__content {
    display: flex;
    align-items: center;
    gap: 62px;
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
        color: #FFFFFF;
        opacity: 0.7;
      }
    }
  }

  &__action {
    width: 240px;
    margin-left: 30px;
  }
}
</style>
