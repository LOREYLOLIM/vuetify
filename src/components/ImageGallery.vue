<template>
  <VCard class="ma-5 my-2 pa-3">
    <VRow>
      <VCol
      v-for="n in 200"
      :key="n"
      cols="4"
      sm="3"
      md="2"
      lg="1"
  
      >
        <VCard
        :elevation="isHovering ? 12 : 2"
        :v-bind = "props"
        @click="1 + 1"
        >
          <v-img
          :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}$greyscale`"
          :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
          aspect-ratio="1"
          class="bg-grey-lighten-2"
          cover
        >
          <template v-slot:placeholder>
            <v-row
              align="center"
              class="fill-height ma-0"
              justify="center"
            >
              <v-progress-circular
                color="grey-lighten-5"
                indeterminate
              ></v-progress-circular>
            </v-row>
          </template>
        </v-img>     
      </VCard>
      </VCol>
    </VRow>
  </VCard>
</template>

<script>
import { defineProps } from 'vue';

const props = defineProps(["isWithColor"])
export default {
  name: "Image Gallery",
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style lang="scss" scoped></style>