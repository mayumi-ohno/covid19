<template>
  <v-app>
    <v-content>
      <Navbar />
      <v-container fluid fill-height>
        <v-row justify="center" align-content="center">
          <router-view></router-view>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar";

export default {
  name: "App",

  components: {
    Navbar
  },
  beforeCreate () {
   this.$store.dispatch("fetchMasterData");
  }
};
</script>
