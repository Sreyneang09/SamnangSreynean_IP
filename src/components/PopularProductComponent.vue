<template>
  <div class="popular-product-container">
    <div class="popular-product" :style="{ backgroundColor: color }">
    <img :src="image" alt="Product Image">
    
    <p class="name">{{ name }}</p>
    <p class="description">{{ description }}</p>
    <p class="rating"> <span v-for="star in 5" :key="star" class="star" :class="{ filled: star <= rating }">&#9733;</span> <span class="rating-number">({{ rating }})</span></p>
    <p class="productWeight">{{ productWeight }} gram</p>
    <div class="price-add"> 
      <p class="price"> 
        <span class="discount-price">{{ discountPrice }}</span> 
        <span class="original-price">{{ originalPrice }}</span> </p> 
        <button v-if="!showQuantity" class="add-button" @click="showQuantityBox">Add +</button> 
         <input v-if="showQuantity" type="number" class="quantity-box" min="1" v-model="quantity" />  </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'PopularProductComponent',
  props: {
    image: String,
    name: String,
    description: String,
    productWeight: Number,
    color: String,
    originalPrice: String,
    discountPrice: String,
    rating: Number
  },
  data() { 
    return { 
      showQuantity: false, 
      quantity: 1 
    }; }, 
  methods: { 
    showQuantityBox() { 
      this.showQuantity = true; 
    } } 
}
</script>

<style scoped>



.popular-product {
  padding: 20px;
  border-radius: 10px;
  
  justify-items: flex-start;
  margin: 10px;
  width: 262px;
  height: 390px;
  border: 1px solid #ccc; 
  transition: border-color 0.3s, box-shadow 0.3s;
}
.popular-product:hover { border-color: #3BB77E; /* Change border color on hover */ box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add shadow on hover */ }
.popular-product img {
  width: 201px;
  height: 144px;
  display: block;
  margin: 0 auto;
  margin-top: 40px;
}
.name { 
  font-size: 12px; 
  color:#7E7E7E;
  font-weight: bold;  } 
.description { 
  font-size: 14px; 
  font-weight: bold;  }
.productWeight{
  font-size: 12px;
  color: #7E7E7E;
  
}
.price-add { 
  display: flex; 
  justify-content: space-between; 
  align-items: center;margin-top: 10px; }
.add-button { 
  margin-left: 80px; 
  cursor: pointer; 
  background: rgb(165, 229, 165); 
  border: none; 
  width: 67px; 
  height: 29px; 
  border-radius: 4px; 
  color:#0ca239;
  transition: background-color 0.3s, box-shadow 0.3s;
} 
.add-button:hover { background-color: #31cb887b; /* Change button color on hover */ box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add shadow on hover */ }
.quantity-box { 
  display: block; 
  margin-top: 10px; 
  width: 67px; 
  height: 29px; 
  margin-left: 80px; }
.price {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  
}
.original-price {
  text-decoration: line-through;
  margin-right: 10px;
  color: #888;
  font-size: 12px;
}
.discount-price {
  color: #3BB77E;
  font-weight: bold;
  font-size: 20px;
}
.rating-number { 
  font-size: 14px;  
  margin-left: 5px; }
.rating { 
  display: flex; 
  justify-content: center; 
  align-items: center; } 
.star { 
  font-size: 20px; 
  color: #ccc; } 
.star.filled { color: #ffd700; }
</style>
