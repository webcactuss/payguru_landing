<script setup lang="ts">
// import { useReveal } from "@/composables/useReveal";
// const { el } = useReveal();
import Container from "../components/Container.vue";
import bgImg from "@/assets/img/DesktopBg.png"
import Button from "@/components/Button.vue";
import HeroBg from "@/assets/img/heroBg.png"
</script>

<template>
  <section class="hero relative overflow-hidden">
    <!-- фон -->
    <div class="hero__bg" />
    <div class="hero__bg-figure" :style="{ backgroundImage: `url(${HeroBg})` }" />
    <Container>
      <div class="hero__content container-page relative pt-10 sm:pt-14 pb-12">
        <div class="hero__content--left">
          <h1 class="hero__title mt-2 text-4xl sm:text-5xl tracking-tight">
            Полный контроль<br class="hidden sm:block" />
            над денежными потоками
          </h1>
          <p class="hero__text mt-4 muted max-w-xl">
            Многофункциональная система оркестрации
            платежей с глобальным покрытием
          </p>
          <div class="mt-6 flex flex-wrap gap-3">
            <Button>Запланировать звонок</Button>
          </div>
        </div>

        <!-- мокап справа -->
        <img class="hero__content-picture" :src="bgImg" alt="">
      </div>
    </Container>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  height: 500px;
  &__bg {
    background: linear-gradient(180deg, rgba(204, 209, 219, 0.7) 0%, rgba(221, 228, 244, 0.7) 97.6%);
    width: 100%;
    position: absolute;
    height: 100%;
  }
  &__bg-figure {
    width: 100%;
    height: 100%;
    position: absolute;
    background-repeat: no-repeat;
    background-size: cover;
  }
  &__content {
    display: flex;
    align-items: end;
    height: 100%;

    &--left {
      min-width: 46%;
      align-self: center;
    }
  }
  &__text {
    line-height: 33px;
    font-size: 24px;
  }
}
</style>
