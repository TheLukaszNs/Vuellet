<template>
  <v-app dark>
    <Navigation/>
    <v-content>
      <v-container>
        <router-view/>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Navigation from "./components/Navigation.vue";

export default {
  components: { Navigation },
  name: "App",
  data() {
    return {
      //
    };
  }
};
</script>
