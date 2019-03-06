<template>
  <div>
    <input type="text" v-model="data.content">
    <br>
    <textarea v-model="data.news" placeholder="asdasdasd"></textarea>
    <br>
    <button @click="Add">Add</button>
    
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      data: {
           image:'',
        content: "",
        news: ""
        
      }
    };
  },
  methods: {
    Add() {
      let url = "https://cs494-5.firebaseio.com/data.json";
      axios.post(url, this.data).then(response => {
        console.log(response);
      });
    },
  }
};
</script>

<style>
</style>
