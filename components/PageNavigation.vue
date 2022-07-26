<template>
  <v-btn-toggle rounded>
    <v-btn nuxt :to="prev">
      <v-icon>mdi-chevron-left</v-icon>
    </v-btn>
    <v-btn>{{ current }}</v-btn>
    <v-btn nuxt :to="next">
      <v-icon>mdi-chevron-right</v-icon>
    </v-btn>
  </v-btn-toggle>
</template>

<script>
export default {
  props: {
    current: String,
    next: String,
    prev: String,
  },
};
</script>

<style></style>
