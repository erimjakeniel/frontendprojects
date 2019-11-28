<template>
  <v-app class="form" id="inspire">
    <v-content>
      <v-container >
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="5">
            <v-card class="elevation-12">
              <v-toolbar color="secondary" dark flat>
                <v-toolbar-title>SIGNUP</v-toolbar-title>
                <v-spacer/>
              </v-toolbar>
              <v-card-text>
                <template>
                  <v-form ref="form" v-model="valid">
                    <v-text-field v-model="name" :rules="nameRules" label="Name" required></v-text-field>
                    <v-text-field v-model="address" :rules="nameRules" label="Address" required></v-text-field>
                    <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
                    <v-text-field
                      v-model="password"
                      :rules="passwordRules"
                      label="Password"
                      type="password"
                      required
                    ></v-text-field>
                    <v-text-field
                      v-model="contact"
                      :rules="numberRules"
                      label="Contact Number"
                      type="number"
                      min="0"
                      required
                    ></v-text-field>
                    <v-text-field v-model="event" :rules="eventRules" label="Event" required></v-text-field>
                    <v-text-field v-model="price" label="Price" type="number" min="1" required></v-text-field>
                    <v-text-field v-model="packages" :rules="packageRules" label="Package" required></v-text-field>
                    <v-text-field v-model="photo" label="Photo" type="file" required></v-text-field>
                  </v-form>
                </template>
              </v-card-text>
              <v-card-actions>
                <v-spacer/>
                <v-btn v-on:click="submit()" color="secondary">Submit</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
// import axios from 'axios'
export default {
  props: {
    source: String
  },
  data: () => ({
    address: "",
    price: "",
    photo: "",

    valid: true,
    name: "",
    nameRules: [v => !!v || "Name is required"],
    contact: "",
    numberRules: [
      v => !!v || "Contact Number is required",
      v => (v && v.length <= 11) || "Name must be less  11 numbers",
      v => (v && v.length >= 11) || "Name must be less  11 numbers"
    ],
    packages: "",
    packageRules: [v => !!v || "Package is important"],
    password: "",
    passwordRules: [
      v => !!v || "password  is required",
      v => (v && v.length >= 8) || "Name must be less  8 numbers"
    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ],
    event: "",
    eventRules: [
      v => !!v || "Event is required",
      v =>
        v == "Birthday" ||
        v == "birthday" ||
        v == "Wedding" ||
        v == "wedding" ||
        v == "Concert" ||
        v == "concert" ||
        "Events must be (Birthday,Wedding or Concert)"
    ]
  }),

  methods: {
    submit() {
      console.log(this.address);
      this.axios
        .post("http://localhost:8000/account", {
          name: this.name,
          address: this.address,
          email: this.email,
          password: this.password,
          contact: this.contact,
          event: this.event,
          price: this.price,
          packages: this.packages
        })
        .then(response => {
          this.$router.push({ path: "Login" });
          console.log(response);
          
        });
    }
  }
};
</script>
<style scoped>
</style>
