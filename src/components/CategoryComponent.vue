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
    background-color: #f0f0f0; 
    padding: 10px;
    margin: 10px;
    text-align: center;
    color: black;
    border-radius: 8px; 
    width: 150px;
    height: 185px;
    box-shadow: 8px 8px 5px rgba(0, 0, 0, 0.1); /* Add shadow */
    transition: transform 0.3s, box-shadow 0.3s;
  
    



  }
  .category:hover { transform: translateY(-10px); /* Pop up effect */ box-shadow: 4px 4px 4px 4px rgba(0, 0, 0, 0.2); /* Darker shadow on hover */ }
  .category img {
    width: 100px;
    height: 100px;
    display: block;
    margin: 0 auto;
  }
  </style>
  
  