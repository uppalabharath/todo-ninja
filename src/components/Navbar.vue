<template>
  <nav>
    <v-toolbar flat app>
      <v-toolbar-side-icon class="grey lighten-4" @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">ToDo</span>
        <span>Ninja</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat color="grey">
        <v-icon left>exit_to_app</v-icon>Sign out
      </v-btn>
    </v-toolbar>
    <!-- navigation drwaer needs a model variable to show and hide -->
    <!-- app prop is mandatory for navigation drwaer to display -->
    <v-navigation-drawer app class="primary" v-model="drawer">
      <v-layout column align-center>
        <v-flex class="mt-4">
          <v-avatar size="100">
            <img src="/avatar-1.png" alt>
          </v-avatar>
          <p class="white--text subheading pt-2">The Net Ninja</p>
        </v-flex>
      </v-layout>
      <v-list>
        <!-- :key binding should point to a value that uniquely identifies the item in list-->
        <v-list-tile v-for="link in links" :key="link.title" router :to="link.route">
          <v-list-tile-action>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">{{ link.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data: function() {
    return {
      drawer: false,
      links: [
        { icon: "dashboard", title: "Dashboard", route: "/" },
        { icon: "folder", title: "My Projects", route: "/projects" },
        { icon: "person", title: "My Team", route: "/team" }
      ]
    };
  }
};
</script>
