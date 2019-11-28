<template>
  <div>
    <v-system-bar color="grey" height="150%"></v-system-bar>
     
        
     
    <!-- <v-app-bar color="grey" dark prominent>
    <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>-->

    <v-spacer></v-spacer>
    

    <!-- </v-app-bar> -->

    <!--  -->
    <template>
      <v-bottom-navigation dark shift>
        
        
        <v-btn icon>
          <span>HOME</span>
          <v-icon @click="goto('/Home')">mdi-home</v-icon>
        </v-btn>
        <v-col cols="12" sm="2" style="margin-top:-20px">
          <v-text-field label="SEARCH" single-line></v-text-field>
        </v-col>

        <v-btn icon >
          <span>Search</span>
          <v-icon v-on:click="searchOne()">mdi-magnify</v-icon>
        </v-btn>
         <v-btn icon style="margin-left:20%">
          <span>Login</span>
          <v-icon @click="goto('/Login')">mdi-login</v-icon>
        </v-btn>
         <v-btn icon >
          <span>Sigup</span>
          <v-icon @click="goto('/Signup')">mdi-clipboard-account</v-icon>
        </v-btn>
      </v-bottom-navigation>
    </template>
  </div>
</template>

   
<script>
export default {
  name: "Sidebar",

  // computed: {
  //   color () {
  //     switch (this.bottomNav) {
  //       case 0: return 'blue-grey'
  //       case 1: return 'teal'
  //       case 2: return 'brown'
  //       case 3: return 'indigo'
  //     }
  //   },
  // },
  methods: {
    goto(link) {
      this.$router.push({ path: link });
    }
  }
  // },
  // data: () => ({
  //   drawer: false,
  //   group: null,
  //   items: [
  //     {
  //       title: "Birthday",
  //       to: "/Birthday "
  //     },
  //     {
  //       title: "Burial",
  //       to: "/Burial"
  //     },
  //     {
  //       title: "Baptist",
  //       to: "/Baptist"
  //     },
  //     {
  //       title: "Wedding",
  //       to: "/Wedding"
  //     }
  //   ]
  // }),
  // methods:{
  //   search(){
  //     axios.get
  //   }
  // },
  // watch: {
  //   group() {
  //     this.drawer = false;
  //   }
  // }
};
</script>
<style scoped>
li {
  display: block;
}

li:hover {
  color: red;
}
</style>



