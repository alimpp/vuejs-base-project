<template>
  <div
    class="home-page d-flex flex-column justify-content-center align-items-center pt-5 px-5 application_animation"
  >
    <h3 class="primary_color">{{ $t("message") }}</h3>
    <p>{{ $t("lorem") }}</p>
  </div>
</template>

<script setup>
import { computed } from "vue";
import { randomString } from "@/plugins/randomString";
import { randomNumber } from "@/utils/randomNumber";

const RandomString = computed(() => {
  return randomString(1000);
});

const RandomNumber = computed(() => {
  return randomNumber(100000000);
});
</script>

<style lang="scss" scoped></style>
