<script setup lang="ts">
import Container from "@/components/Container.vue";
import WebIcon from "@/assets/img/icons/web.svg";
import Background from "@/assets/img/map.png"
import Check from "@/assets/img/icons/Check.svg"
import {ref} from "vue";

const items = ref([
  {
    text: "Поддержка локальных методов, <br /> банков и валют."
  },
  {
    text: "Маршрутизация по GEO, валюте, банку <br /> или платёжной системе получателя, диапазону сумм и рисковому профилю."
  },
  {
    text: "Гибкая каскадная логика между исполнителями."
  },
  {
    text: "Трансграничные сценарии, конвертация, <br /> многоступенчатые лимиты."
  }
])
</script>

<template>
  <section class="geography">
    <div class="geography__background" :style="{ backgroundImage: `url(${Background})` }" />
    <Container>
      <div>
        <h2>География и покрытие</h2>
        <div class="geography__card">
          <div class="">Мы работаем на всех континентах</div>
          <div class="flex justify-between align-baseline">
            <div>50+ стран</div>
            <img alt="icon" :src="WebIcon" />
          </div>
        </div>
        <div class="geography__list">
          <div v-for="item in items" class="geography__list-item">
            <img class="geography__list-item-check" :src="Check"  />
            <div class="geography__list-item-text" v-html="item.text" />
          </div>
        </div>
      </div>
      <div class="geography__image-bg" :style="{ backgroundImage: `url(${Background})` }" />
    </Container>
  </section>
</template>

<style scoped lang="scss">
.geography {
  background: #091734;
  color: #fff;
  padding: 100px 0;
  position: relative;

  &__card {
    width: 382px;
    padding: 24px;
    border-radius: 20px;
    border: 1px solid #1D65FF;
    margin-top: 60px;
    //background: linear-gradient(90deg, #1D65FF 0%, #00329C 50%, #00329C 100%);
  }

  &__list {
    display: flex;
    flex-direction: column;
    gap: 40px;
    max-width: 563px;
    margin-top: 60px;

    &-item {
      display: flex;
      gap: 10px;

      &-check {
        width: 24px;
        height: 24px;
      }
      &-text {
        font-size: 21px;
        color: #627286;
      }
    }
  }

  &__image-bg {
    position: absolute;
    width: 1025px;
    height: 560px;
    top: 176px;
    right: 100px;
    background-size: contain;
    background-repeat: no-repeat;
  }
}
</style>
