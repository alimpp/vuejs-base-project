<template>
  <div class="index-layout">
    <desktopNav class="desktop-size" />
    <mobileNav class="mobile-size" />
    <router-view></router-view>
  </div>
</template>

<script setup>
import mobileNav from "@/layout/base/mobileNav";
import desktopNav from "@/layout/base/desktopNav";
import footer from "@/layout/base/footer";
</script>

<style lang="scss" scoped>
.index-layout {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  .mobile-size {
    display: none;
  }
  @media (max-width: 900px) {
    .desktop-size {
      display: none;
    }
    .mobile-size {
      display: inline;
    }
  }
}
</style>
