<template>

  <div id="bg">
    <span >
  
</span>
    <v-container fluid>
      <v-row dense>
        <v-col cols="6" sm="4">
          <v-card>
            <v-img
              src="../assets/wed.png"
              class="white--text align-end"
            
              height="300px"
            >
            <v-card-title>WEDDING</v-card-title>
            </v-img>
            <v-card-actions>
                <v-btn color="primary" v-on:click="Wedding()">Visit</v-btn>
              <v-spacer></v-spacer>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="6" sm="4">
          <v-card>
            <v-img
              src="../assets/cons.jpg"
              class="white--text align-end"
            
              height="300px"
            >
            <v-card-title>CONCERT</v-card-title>
            </v-img>
            <v-card-actions>
               <v-btn v-on:click="concert()" color="secondary">Visit</v-btn>
              <v-spacer></v-spacer>          
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="6" sm="4">
          <v-card>
            <v-img
              src="../assets/ber.jpg"
              class="white--text align-end"
            
              height="300px"
            >
            <v-card-title>BIRTHDAY PARTY</v-card-title>
            </v-img>
            <v-card-actions>
              <v-btn color="primary" v-on:click="Birthday()">Visit</v-btn>
              <v-spacer></v-spacer>
            
            </v-card-actions>
          </v-card>
        </v-col>
        
      </v-row>

    </v-container>
    <hr>
    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="6" sm="6">
            <v-img src="../assets/wed1.png"></v-img>
          </v-col >
          <v-col cols="6" sm="6">
          <h1>The day I meet you i found my missing piece.<br>You complete me and make me a better person.<br> I love you with all my heart and all my soul </h1>
          </v-col >
        </v-row>
      </v-container>
    </template>

    <hr/>
      <template>
     
      <v-container fluid>
     <v-row>
        <v-col cols="6" sm="6">
          <h1 id="left">The day I meet you i found my missing piece.<br>You complete me and make me a better person.<br> I love you with all my heart and all my soul </h1>
          </v-col>
          <v-col cols="6" sm="6">
            <v-img src="../assets/wed1.png"></v-img>
          </v-col>
          </v-row>
      </v-container>
    </template>
    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="6" sm="6">
            <v-img src="../assets/wed1.png"></v-img>
          </v-col >
          <v-col cols="6" sm="6">
          <h1>The day I meet you i found my missing piece.<br>You complete me and make me a better person.<br> I love you with all my heart and all my soul </h1>
          </v-col >
        </v-row>
      </v-container>
    </template>
    
  </div>
</template>
<script>
export default {
 
  methods:{
    concert(){
       this.$router.push({ path: "Concert" });
      
    }, Birthday(){
       this.$router.push({ path: "Birthday" });
      
    },
    Wedding(){
       this.$router.push({ path: "Wedding" });
      
    }
  }
    
  
}
</script>



<style scoped>
.bottom-gradient {
  background-image: linear-gradient(
    to top,
    rgba(0, 0, 0, 0.4) 0%,
    transparent 72px
  );
}

.repeating-gradient {
  background-image: repeating-linear-gradient(
    -45deg,
    rgba(255, 0, 0, 0.25),
    rgba(255, 0, 0, 0.25) 5px,
    rgba(0, 0, 255, 0.25) 5px,
    rgba(0, 0, 255, 0.25) 10px
  );
}
p {
  font-size: 30px;
  color: yellow;
}
h1 {
  float: right;
  position: responsive;
  margin-top: 20px;
  text-align:center
}
#left{
  float:left
}
#bg{
  height: 100%;
  width:100%;
  top:0;
  bottom:0;
  background-image: url("../assets/wed.jpg");
  background-size: cover;
  
}
</style>