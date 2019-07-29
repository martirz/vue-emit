<template>
  <v-layout align-center justify-center row >
    <v-btn v-on:click="$emit('togglePlay', !playing)">{{ playIcon }}</v-btn>
  </v-layout>
</template>

<script>
export default {
  name: "PlayerControl",
  props: {
    'playIcon': String,
    'playing': Boolean
  },
  data() {
    return {
    }
  },
  methods: {
  }
};
</script>

<style scoped></style>
