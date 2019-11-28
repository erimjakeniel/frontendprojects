<template>
  <div>
    <v-system-bar color="deep-purple darken-3"></v-system-bar>
    <v-app-bar color="grey accent-4" dark prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <h2 style="float:left">ABout</h2>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute bottom temporary height="60%">
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-avatar size="100" style="margin-left:30%">
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
          </v-avatar>
          <center>
            <h2>WeOrg!</h2>
          </center>
          <br>
          <hr>
          <v-list-item>
            <router-link to="/viewporfolio">VIEW PORFOLIO</router-link>
          </v-list-item>

          <v-list-item>
            <router-link to="/updateporfolio">UPDATE PORFOLIO</router-link>
          </v-list-item>
          <v-list-item>
            <router-link to="/">LOGOUT</router-link>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <div>
      <v-card style="margin-right:5%;margin-left:5%;margin-top:5%;background-color:grey">
        <br>
        <h2 style="text-align:center;margin-top:2%">ABOUT</h2>
        <template v-slot:default>
          <v-container fluid>
            <v-data-table :headers="headers" :items="org"></v-data-table>
            <v-btn v-on:click="searchOne()">VIEW</v-btn>
            <v-btn v-on:click="edit()">EDIT</v-btn>
          </v-container>
          <template>
            <v-row style="width:90%;margin-left:5%;margin-right:5%;margin-top:5%">
              <v-col>
                <v-card>
                  <v-container fluid>
                    <h2>My Porfolio</h2>
                    <v-row>
                      <v-col v-for="n in 9" :key="n" class="d-flex child-flex" cols="4">
                        <v-card flat tile class="d-flex">
                          <v-img
                            :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                            :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                            aspect-ratio="1"
                            class="grey lighten-2"
                          >
                            <template v-slot:placeholder>
                              <v-row class="fill-height ma-0" align="center" justify="center">
                                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                              </v-row>
                            </template>
                          </v-img>
                        </v-card>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-card>
              </v-col>
            </v-row>
          </template>
        </template>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "personalAccount",
  data() {
    return {
      org: [],
      headers: [
        {
          text: "Name",

          align: "left",
          sortable: false,
          value: "name"
        },

        { text: "Address", value: "address" },
        { text: "Contact", value: "contact" },
        { text: "Email", value: "email" },
        { text: "Event", value: "event" },
        { text: "Packages", value: "packages" },
        { text: "Price", value: "price" }
      ]
    };
  },
  // watch: {
  //   group() {
  //     this.drawer = false;
  //   }
  // },
  methods: {
    searchOne() {
      var org = [];
      var name = "MellyneGrace";
      this.axios
        .post("http://localhost:8000/retrieveOne/" + name)
        .then(response => {
          console.log(response);
          var dataT = response.data;
          // this.org = dataT
          org.push({
            name: dataT.name,
            address: dataT.address,
            contact: dataT.contact,
            email: dataT.email,
            event: dataT.event,
            packages: dataT.packages,
            price: dataT.price
          });

          // console.log(org);
          this.org = org;
          alert(org);
        })
        .catch(error => {
          console.log(error);
        });

      return org;
    },
    edit() {
      var org = [];
      var name = "MellyneGrace";
      this.axios
        .post("http://localhost:8000/retrieveOne/" + name)
        .then(response => {
          console.log(response);
          var dataT = response.data;
          // this.org = dataT
          org.push({
            name: dataT.name,
            address: dataT.address,
            contact: dataT.contact,
            email: dataT.email,
            event: dataT.event,
            packages: dataT.packages,
            price: dataT.price
          });

          // console.log(org);
          this.org = org;
          alert(org);
        })
        .catch(error => {
          console.log(error);
        });

      return org;
    }
  }
};
</script>


