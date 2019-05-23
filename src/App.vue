<template>
  <v-app class="grey lighten-4">
    <c-navbar/>
    <v-content class="mx-4">
      <!-- The following loads the output of the router navigation-->
      <router-view></router-view>
    </v-content>
  </v-app>
</template>
<script>
import Navbar from "@/components/Navbar";
export default {
  name: "App",
  components: {
    cNavbar: Navbar
  },
  data() {
    return {
      //
    };
  }
};
</script>
