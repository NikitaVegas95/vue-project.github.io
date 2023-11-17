<script setup lang="ts">
import LayoutHeader from "./components/Header/LayoutHeader.vue";
import LayoutContent from "@/components/Content/LayoutContent.vue";
import LayoutFooter from "@/components/Footer/LayoutFooter.vue";
</script>

<template>
  <div class="wrapper">
    <LayoutHeader/>
    <LayoutContent/>
    <LayoutFooter/>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
}
.content {
  flex-grow: 1;
}
</style>
