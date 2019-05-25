<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>
    <!-- container keeps the content center aligned. If need to use full width we can use fluid prop -->
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="member in team" :key="member.name">
          <v-card flat class="text-xs-center ma-2">
            <!-- using v-responsive for images -->
            <v-responsive class="pt-3">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="member.avatar" alt>
              </v-avatar>
            </v-responsive>
            <!-- card content -->
            <v-card-text>
              <div class="subheading">{{ member.name }}</div>
              <div class="grey--text">{{ member.role }}</div>
            </v-card-text>
            <!-- card actions -->
            <v-card-actions>
              <v-btn small flat color="grey">
                <v-icon left>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      team: [
        {
          name: "The Net Ninja",
          role: "Web developer",
          avatar: "/avatar-1.png"
        },
        { name: "Ryu", role: "Graphic designer", avatar: "/avatar-2.png" },
        { name: "Chun Li", role: "Web developer", avatar: "/avatar-3.png" },
        {
          name: "Gouken",
          role: "Social media maverick",
          avatar: "/avatar-4.png"
        },
        { name: "Yoshi", role: "Sales guru", avatar: "/avatar-5.png" }
      ]
    };
  }
};
</script>
