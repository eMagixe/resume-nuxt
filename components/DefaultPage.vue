<template>
  <v-card>
    <v-img class="white--text align-end" height="330px" :src="image">
      <v-card-title>
        <v-spacer></v-spacer>
        <page-navigation :current="upperTitle" :prev="prev" :next="next" />
      </v-card-title>
    </v-img>
    <v-card-text>
      <slot></slot>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    title: String,
    image: String,
    prev: String,
    next: String,
  },
  computed: {
    upperTitle() {
      return this.title.toUpperCase();
    },
  },
};
</script>
