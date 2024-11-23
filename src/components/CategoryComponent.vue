<template>
    <div class="category" :style="{ backgroundColor: color }">
      <img :src="image" alt="Category Image">
      <p>{{ name }} </p>
      <p>({{ quantity }} items)</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CategoryComponent',
    props: {
      image: String,
      name: String,
      quantity: Number,
      color: String
    }
  }
  </script>
  
  <style scoped>
  .category {
    background-color: #f0f0f0; /* Change this to your desired background color */
    border: 1px solid #ccc; /* Frame or box around the photo */
    padding: 10px;
    margin: 10px;
    text-align: center;
    color: black;
    border-radius: 8px; /* Rounded corners */
    width: 150px;
    height: 185px;
    
  
    



  }
  .category img {
    width: 100px;
    height: 100px;
    display: block;
    margin: 0 auto;
  }
  </style>
  
  