<template>
  <v-app>
    <Header v-if="loginNa()" />
    <router-view />
    <template>
  <v-footer color="silver">
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
</template>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",

  components: {
    Header
  },

  data: () => ({
    //
  }),
  methods: {
    loginNa() {
      if (this.$route.path == "/personalAccount") {
        return false;
      }
       else if (this.$route.path == "/updateporfolio") {
        return false;
      } 
      else if (this.$route.path == "/viewporfolio") {
        return false;
      } else {
        return true;
      }
    }
  }
};
</script>
