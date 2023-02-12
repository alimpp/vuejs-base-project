<template>
  <div
    class="home-page d-flex flex-column justify-content-center align-items-center pt-5 px-5"
  >
    <h3 class="primary_color">{{ $t("message") }}</h3>
    <p>{{ $t("lorem") }}</p>
    <div class="d-flex">
      <h6 class="py-2 px-2">{{ $t("randompass") }} =></h6>
      <h6 class="px-3 py-2 primary_background rounded">{{ RandomString }}</h6>
    </div>
    <div class="d-flex">
      <h6 class="py-2 px-2">{{ $t("randompass") }} =></h6>
      <h6 class="px-3 py-2 primary_background rounded">{{ RandomNumber }}</h6>
    </div>
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
