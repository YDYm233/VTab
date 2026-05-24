<script setup lang="ts">
import { ref } from "vue"
import { useRouter } from "vue-router"
const router = useRouter()
const active = ref(0)
</script>

<template>
  <div id="vtab-app">
    <var-app-bar title="V_Tab" title-position="center" color="#1e1e2e">
      <template #left>
        <var-icon name="menu" @click="active = active === 1 ? 0 : 0" />
      </template>
      <template #right>
        <var-icon name="brightness-6" />
      </template>
    </var-app-bar>

    <router-view />

    <var-bottom-navigation v-model:active="active" borderless>
      <var-bottom-navigation-item
        label="首页"
        icon="home-outline"
        @click="router.push('/')"
      />
      <var-bottom-navigation-item
        label="关于"
        icon="information-outline"
        @click="router.push('/about')"
      />
      <var-bottom-navigation-item label="收藏" icon="heart-outline" />
      <var-bottom-navigation-item label="设置" icon="cog-outline" />
    </var-bottom-navigation>
  </div>
</template>

<style scoped>
#vtab-app {
  min-height: 100vh;
}
</style>
