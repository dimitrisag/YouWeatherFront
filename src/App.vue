<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar>
      <v-app-bar-nav-icon :icon="mdiMenu" @click.stop="drawer = !drawer">
      </v-app-bar-nav-icon>
      <v-app-bar-title>
        <img src="@/assets/youweather.png" alt="logo" height="80" class="pa-2">
      </v-app-bar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <nav-menu></nav-menu>
    </v-navigation-drawer>

    <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
      Main Content
    </v-main>
  </v-layout>
</template>

<script>
import NavMenu from '@/components/menus/NavMenu.vue'
import { mdiMenu } from '@mdi/js'
export default {
  name: 'App',
  components: {
    NavMenu
  },
  data: () => ({
    drawer: false,
    mdiMenu
  })
}
</script>