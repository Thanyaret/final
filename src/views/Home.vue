<template>
  <div class="home">
    <Navbar></Navbar>


  <br>
  <br>
    <h1 class="text-center display-3 ">เดินทางมามหาวิทยาลัย 140 คน</h1><br>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs20 sm8 md8 lg3 v-for ="person in home" :key="person.name">
        <v-card color="purple lighten-2" class=" ma-5">
        <v-card-text>
        <div class="headline">{{person.name}}</div><br>
        <div class="subtitle">{{person.time}}</div><br>
        <v-divider class="mx-4"></v-divider><br>
        <div class="display-3 text-center">{{person.role}}</div><br>     
        </v-card-text>
        </v-card>    
        </v-flex> 
      </v-layout>
    </v-container>
  </div>
</template>
<script>
import Navbar from "../components/Navbar"
export default {
  components: {Navbar},
  data(){
    return{
      home: [
        {name: 'ตึก ICT',role:'35 คน',time:'Mon, 12:30 PM'},
        {name: 'ตึก PKY',role:'35 คน',time:'Mon, 12:30 PM'},
        {name: 'ตึก CE',role:'35 คน',time:'Mon, 12:30 PM'},
        {name: 'ตึก EN',role:'35 คน',time:'Mon, 12:30 PM'},
      ]
    }
  }

}
</script>
