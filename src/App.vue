<script setup>
import SideBarVue from './components/SideBar.vue';
import ImageGallery from './components/ImageGallery.vue';

import {ref} from "vue"

const isWithColor = ref(true)

const onSelectOption = (isColor) => {
  isWithColor.value = isColor
}
</script>
<template>
  <v-app>
    {{isWithColor}}
     <SideBarVue @selectOption="onSelectOption">
      
     </SideBarVue>
    <v-main>
       <ImageGallery :isWithColor="isWithColor"></ImageGallery>
    </v-main>
  </v-app>
</template>

