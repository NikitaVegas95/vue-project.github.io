<script setup lang="ts">
import { ref } from 'vue'
import type { IThemes } from '@/components/Header/LayoutHeader.types'

const themes = ref<IThemes>({
  isWhite: false
})

const changeTheme = () => {
  themes.value.isWhite = themes.value.isWhite === 'blackTheme' ? 'whiteTheme' : 'blackTheme'
}
</script>

<template>
  <header :class="themes.isWhite" class="header">
    <v-btn @click="changeTheme"> Button </v-btn>
  </header>
</template>

<style scoped lang="scss">
.header {
  height: 150px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 32px;
  font-weight: 700;
}

.whiteTheme {
  background-color: white;
  color: black;
  transition:
    background-color ease-in-out 0.3s,
    color ease-in-out 0.3s;
}

.blackTheme {
  background: black;
  color: white;
  transition:
    background-color ease-in-out 0.3s,
    color ease-in-out 0.3s;
}
</style>
