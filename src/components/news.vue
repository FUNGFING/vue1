<template>
  <div>
    
       <div v-for="(d,index) in Info" :key="index">
   <center> <b-card bg-variant="info" text-variant="white" :title=d.IOD style="max-width: 540px;">
            
      
      <p class="card-text">{{d.first_name}}</p>
      <p class="card-text">{{d.last_name }}</p>
      <p class="card-text">{{d.email}}</p>
      <p class="card-text">{{d.first_name}}</p>
      <p class="card-text">{{d.ip_address}}</p>
      <b-button href="#" variant="success"></b-button>
    </b-card>
    </center>
    <br>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      Info: []
    };
  },
  mounted() {
    axios.get("https://cs494-5.firebaseio.com/data.json").then(response => {
      const data = response.data;
      for (let key in data) {
        const info = data[key];
        info.id = key;
        this.Info.push(info);
      }
    });
  }
};
</script>

<style>
</style>
