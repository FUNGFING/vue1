<template>
  <div><center>
    <b-card class="bv-example-row" bg-variant="info" text-variant="Dark" :title=d.IOD  style="max-width: 900px;">
    <b-row>
        <b-col></b-col>
        <b-col>
          เพิ่มข้อมูล
           <b-form-input v-model="data.IOD" type="text" placeholder="id"></b-form-input>
            <b-form-input v-model="data.first_name" type="text" placeholder="first_name"></b-form-input>
             <b-form-input v-model="data.last_name" type="text" placeholder="last_name"></b-form-input>
              <b-form-input v-model="data.email" type="text" placeholder="email"></b-form-input>
              <b-form-input v-model="data.gender" type="text" placeholder="gender"></b-form-input>
              <b-form-input v-model="data.ip_address" type="text" placeholder="ip_address"></b-form-input>
           <br>
           
           
    <button @click="Add">Add</button>
        </b-col>
        <b-col></b-col>
    </b-row>
    </b-card>
</center>
  
  </div>
</template>



<script>
import axios from "axios";
export default {
  data() {
    return {
      
      data: {
        
        IOD : "" ,
      first_name : "",
  last_name : "",
  email : "",
  gender : "",
  ip_address : "",
  
      }
    };
  },
  methods: {
    Add() {
      let url = "https://cs494-5.firebaseio.com/data.json";
      axios.post(url, this.data).then(response => {
        console.log(response);
        alert('Add Success !!')
        
        this.data.IOD
      this.data.first_name
  this.data.last_name 
  this.data.email 
  this.data.gender 
  this.data.ip_address 
      });

    }

  }
};
</script>

<style>
</style>
