<template>
  <div id="bg">
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
  <v-carousel hide-delimiters style="height:70vh;">
    <v-carousel-item fluid  style="width:100%;height:800px;"
      v-for="(item,i) in items" 
      :key="i"
      :src="item.src"
      
    ></v-carousel-item>
  </v-carousel>
</template>

    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/con1.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4>When you go to a concert, part of being there is that you're all hearing the same thing. It's about being in a crowd. If you go to a gig and there are two people there, then it's not the same thing. </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>
    

      <template>
      <v-container fluid>
     <v-row>
        <v-col cols="12" sm="6">
          <h4 >The love you've shown me is beyond anything my childhood self could dream up. Its heartwarming , genuine and fierce sometimes all at once. At the same time your love has taught me to find what I spent to long  searching for within my own self. </h4>
          </v-col>
          <v-col cols="12" sm="6">
            <v-img src="../assets/wedding1.jpg"></v-img>
          </v-col>
          </v-row>
      </v-container>
    </template>

    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/con2.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4> Heres to the night that tured into morning, and the friends who turned into family. </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>

    <template>
     
     <v-container fluid>
    <v-row>
       <v-col cols="12" sm="6">
         <h4 >I mean, eighteen years old is the age of consent in Europe and you can go anywhere and do anything you like. In America, it is dumb. At eighteen you should be able to do anything that you like, except get married. </h4>
         </v-col>
         <v-col cols="12" sm="6">
           <v-img src="../assets/bday3.jpg"></v-img>
         </v-col>
         </v-row>
     </v-container>
   </template>

    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/bday2.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4>Dance like the whole world is your stage and every day is your debut. </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>

    <template>
     
      <v-container fluid>
     <v-row>
        <v-col cols="12" sm="6">
          <h4 >Music touches us emotionally where words cant!</h4>
          </v-col>
          <v-col cols="12" sm="6">
            <v-img src="../assets/con4.jpg"></v-img>
          </v-col>
          </v-row>
      </v-container>
    </template>

    <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/wedv1.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4>Your task is not to seek for love, but merely to seek and find all the barriers within yourself that you have built against it. </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>


   <template>
      <v-container fluid>
     <v-row>
        <v-col cols="12" sm="6">
          <h4 >Count your life by smiles, not tears. Count your age by friends, not years. Happy birthday! </h4>
          </v-col>
          <v-col cols="12" sm="6">
            <v-img src="../assets/bday1.png"></v-img>
          </v-col>
          </v-row>
      </v-container>
    </template>


   <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/bday4.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4>Birthdays are a new start, a fresh beginning and a time to pursue new endeavors with new goals. Move forward with confidence and courage. You are a very special person. May today and all of your days be amazing! </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>

    <template>
     
     <v-container fluid>
    <v-row>
       <v-col cols="12" sm="6">
         <h4 >Everyday we make more progress towards understanding  the concert hall.</h4>
         </v-col>
         <v-col cols="12" sm="6">
           <v-img src="../assets/con3.jpg"></v-img>
         </v-col>
         </v-row>
     </v-container>
   </template>

   <template>
  <v-container fluid>
        <v-row>
          <v-col cols="12" sm="6">
            <v-img src="../assets/wedf.jpg"></v-img>
          </v-col >
          <v-col cols="12" sm="6">
          <h4>The day I meet you i found my missing piece.<br>You complete me and make me a better person.<br> I love you with all my heart and all my soul </h4>
          </v-col >
        </v-row>
      </v-container>
    </template>
  
  </div>
</template>
<script>
export default {
  data () {
    return {
      items: [
        {
          src: 'https://i.pinimg.com/originals/3e/a7/78/3ea778fa9872c262fda16c677e78c26e.jpg'
        },
        {
          src: 'https://www.theblueleaf.com/wp-content/uploads/2019/01/18-roses-unique-ideas-to-try-on-your-debut-1200x800.png'
        }, 
      
        {
          src: 'https://1hq6f244nzqssy4d8fp6y7re-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/elegant-wedding-regal-wedding-with-red-gold-details1.jpg'
        },
        {
          src: 'https://s.yimg.com/ny/api/res/1.2/lunUeHZSJZFU95Ulw5Zs.Q--~A/YXBwaWQ9aGlnaGxhbmRlcjtzbT0xO3c9ODAw/http://media.zenfs.com/en-US/homerun/realtor_com_80/0f3008ff0920d04de0f803ebb67b6616'
        }, 
        {
          src: 'https://www.straitstimes.com/sites/default/files/articles/2014/05/08/ST_20140508_LIFBEEP_300600e_2x.jpg'
        },
        {
          src: 'https://www.mccarthyevents.com/wp-content/uploads/Batty-Tent-Interior-1-1600x1067.jpg'
        },
        {
          src: 'https://i.pinimg.com/originals/32/17/96/321796c217c3fa93013944de4772e7f8.jpg'
        },
        {
          src: 'https://www.teragramballroom.com/files/2015/03/DANDY-WARHOLS-TERAGRAM-12-05-15-5.jpg'
        }, 
        {
          src: 'https://hizonscatering.com/wp-content/uploads/2018/03/Debut-Reception.jpg'
        },
        {
          src: 'https://www.regalhotel.com/uploads/rah/meetings_n_events/wedding/720x475/wedding5.jpg'
        }, 
        {
          src: 'https://primovenues.com/wp-content/uploads/2016/08/Best-Events-Dusit-Thani-Manila.jpg'
        }, 
        
      ]
    }
  },
 
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
h4 {
  margin-top:20%;
  font-size: 25px;
  font-style:Medium italic;
  text-align:center;
  position: responsive;

}
#left{
  float:left
}
#bg{
  height: 100%;
  width:100%;
  top:0;
  bottom:0;
  /* background-color: #F0C5D5; */
  background-image: url("../assets/wedbck.jpg");
  background-size: cover;
  background-repeat: no-repeat
  
}

</style>  