<template>
  <div></div>
  <VNavigationDrawer 
    expand-on-hover 
    rail
  >
    <v-list>
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
        subtitle="lorex@gmailcom"
        title="Lorex Dev"
      ></v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item prepend-icon="mdi-image" title="Color Gallery" value="color" @click="selectOption(true)"></v-list-item>
      <v-list-item prepend-icon="mdi-dialpad" title="Grey Gallery" value="color" @click="selectOption(false)"></v-list-item>

      <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
      <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
    </v-list>

  <v-main style="height: 250px"></v-main>

  </VNavigationDrawer>
</template>

<script>
import { defineEmits } from 'vue';

const emits = defineEmits(['selectOption'])
const selectOption = (isColor) => {
  emits("selectOption", isColor)
}
export default {
  name: "SideBar",

  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style lang="scss" scoped></style>