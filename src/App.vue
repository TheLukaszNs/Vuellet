<template>
  <v-app>
    <Navigation/>
    <v-content></v-content>
  </v-app>
</template>

<script>
import Navigation from './components/Navigation.vue';

export default {
  components: { Navigation },
  name: 'App',
  data() {
    return {
      //
    };
  },
};
</script>
