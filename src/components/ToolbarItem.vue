<template>
  <v-btn flat color="grey mr-2">
    <v-icon left>{{ icon ? icon : null }}</v-icon>
    <span>{{ title }}</span>
  </v-btn>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    icon: {
      type: String
    }
  }
};
</script>
