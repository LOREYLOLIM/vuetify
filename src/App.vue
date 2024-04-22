<template>
  <v-app>
    <!-- Sidebar -->
    <SideBar @selectOption="onSelectOption"/>
    <v-main>
      <!-- card -->
      <ImageGallery :isWithColor="isWithColor"/>
    </v-main>
  </v-app>
</template>

<script>
import SideBar from '@/components/SideBar'
import ImageGallery from './components/ImageGallery.vue'
import { ref } from 'vue';

const isWithColor = ref(true)
const onSelectOption = (isColor) => {
  isWithColor.value = isColor
}
export default {
  name: 'App',

  components: {
    SideBar,
    ImageGallery,
  },

  data: () => ({
    //
  }),
}
</script>
