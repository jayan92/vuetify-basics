<template>
  <v-app>
    <navigation-drawer @selectOption="onSelectOption" />

    <v-main>
      <image-gallary :isWithColor="isWithColor" />
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue";

import NavigationDrawer from "./components/NavigationDrawer.vue";
import ImageGallary from "./components/ImageGallary.vue";

const isWithColor = ref(true);

const onSelectOption = (isColor) => {
  isWithColor.value = isColor;
};
</script>
