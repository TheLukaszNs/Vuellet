<template>
  <nav>
    <v-toolbar flat app>
      <v-toolbar-title class="text--uppercase grey--text">
        <span>Vue</span>
        <span class="font-weight-light">llet</span>
      </v-toolbar-title>
      <v-spacer/>
      <v-toolbar-items>
        <ToolbarItem v-for="link in links" :key="link.title" :title="link.title" :icon="link.icon"/>
      </v-toolbar-items>
    </v-toolbar>
    <v-navigation-drawer floating permanent app mini-variant>
      <v-toolbar flat/>
      <v-list dir class="mt-2 pt-0">
        <v-list-tile v-for="link in links" :key="link.title" @click>
          <v-list-tile-action>
            <v-icon>{{ link.icon }}</v-icon>
          </v-list-tile-action>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer class="pa-3" app>
      <v-spacer/>
      &copy; {{ new Date().getFullYear() }} - Łukasz Myśliwiec
    </v-footer>
  </nav>
</template>

<script>
import ToolbarItem from "./ToolbarItem";
export default {
  components: { ToolbarItem },
  data() {
    return {
      // TODO: Add actual links
      links: [
        {
          title: "Create Wallet",
          icon: "mdi-pencil"
        },
        {
          title: "Add Goal",
          icon: "mdi-plus-circle"
        },
        {
          title: "Settings",
          icon: "mdi-settings"
        }
      ]
    };
  }
};
</script>
