<script setup lang="ts">
const theme = computed(() => isDark.value ? 'dark' : 'light')
</script>

<template>
  <v-responsive>
    <v-app :theme="theme">
      <v-app-bar-nav-icon />
      <v-app-bar class="px-3">
        <v-spacer />
        <HeaderTool />
      </v-app-bar>
      <v-main>
        <v-container>
          <RouterView />
        </v-container>
      </v-main>
    </v-app>
  </v-responsive>
</template>
