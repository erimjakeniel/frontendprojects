<template>
<div>
  <v-app class="form" id="inspire">
    <v-content>
      <v-container style="margin-top:-10%">
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="secondary" dark flat>
                <v-toolbar-title>LOGIN</v-toolbar-title>
                <v-spacer />
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field
                    v-model="email"
                    label="Email"
                    name="login"
                    prepend-icon="mdi-account"
                    type="text"
                    :rules="emailRules"
                    required
                  ></v-text-field>
                  <v-text-field
                    v-model="password"
                    id="password"
                    label="Password"
                    name="password"
                    prepend-icon="mdi-lock"
                    type="password"
                    :rules="passwordRules"
                    required
                  ></v-text-field>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn v-on:click="login" color="secondary">Login</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
  </div>
</template>


<script>
import axios from "axios";

export default {
  name: "btnLogin",
  data: () => ({
    valid: true,
    password: "",
    passwordRules: [
      v => !!v || "password  is required",
      v => (v && v.length >= 8) || "Name must be less  8 numbers"
    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ]
  }),
  methods: {
    login() {
      axios
        .post("http://localhost:8001/login", {
          username: this.email,
          password: this.password
        })
        .then(response => {
          this.$router.push({ path: "personalAccount" });
          console.log(response)
        });
    }
  },
  props: {}
};
</script>
<style scoped>
.form {
  margin-top: 15%;
}
</style>
