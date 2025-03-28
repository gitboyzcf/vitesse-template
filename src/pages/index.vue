<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
})
const { t } = useI18n()

// const user = useUserStore()
// const name = ref(user.savedName)

// const router = useRouter()
// function go() {
//   if (name.value)
//     router.push(`/hi/${encodeURIComponent(name.value)}`)
// }

const drawer = ref(true)

useHead({
  title: () => t('button.home'),
})
</script>

<template>
  <v-navigation-drawer
    v-model="drawer" location="right"
  >
    <v-file-input label="File input" variant="solo" />
  </v-navigation-drawer>
  <div>
    1111
    <v-fab :icon="drawer ? 'i-carbon-chevron-right' : 'i-carbon-chevron-left'" app />
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
