<template>
    <div class="product">
      <img :src="image" alt="Product Image">
      <p>{{ name }} ({{ quantity }} items)</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductComponent',
    props: {
      image: String,
      name: String,
      quantity: Number
    }
  }
  </script>
  
  <style scoped>
  .product {
    display: inline-block;
    text-align: center;
    margin: 10px;
  }
  .product img {
    width: 100px;
    height: 100px;
  }
  </style>
  