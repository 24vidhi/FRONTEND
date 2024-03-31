<script setup lang="ts">
import { RouterView } from 'vue-router'

</script>

<template>
  <!-- NAV BAR == present in all the pages -->
  <v-card
    color="grey-lighten-6"
    rounded="0"
    flat
  >
    <v-toolbar color="blue-lighten-4" density="compact">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Chat App</v-toolbar-title>

      <v-spacer></v-spacer>
    </v-toolbar>
  </v-card>
  <RouterView />
</template>
