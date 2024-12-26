<template>
  <div id="app">
    <header> 
      <nav class="navbar"> 
        <ul class="nav-list"> 
          <li class="nav-item"><a href="#">All</a>
          </li> <li class="nav-item"><a href="#">Milks & Dairies</a>
          </li> <li class="nav-item"><a href="#">Coffees & Teas</a>
          </li> <li class="nav-item"><a href="#">Pet Foods</a></li> 
          <li class="nav-item"><a href="#">Meats</a>
          </li> <li class="nav-item"><a href="#">Vegetables</a></li> 
          <li class="nav-item"><a href="#">Fruits</a></li> 
        </ul> </nav> 
      </header>
    
      <div class="main-container">
      
       <div class="category-section"> <h> Category Component</h> 
         <div class="category-container"> <CategoryComponent v-for="(product, index) in categoryProducts" :key="index" :image="product.image" :name="product.name" :quantity="product.quantity" :color="product.color" /> </div>
         </div >
       <div class="promotion-section">
       <h>Promotion Component</h>
       <div class="promotion-container"> <PromotionComponent :items="promotionItems" />
       </div>
    </div>
    <div class="header-container"> 
      <h2 class="popular-product-header">Popular Product</h2> <nav class="navbar"> <ul class="nav-list"> <li class="nav-item"><a href="#">All</a></li> <li class="nav-item"><a href="#">Milks & Dairies</a></li> <li class="nav-item"><a href="#">Coffees & Teas</a></li> <li class="nav-item"><a href="#">Pet Foods</a></li> <li class="nav-item"><a href="#">Meats</a></li> <li class="nav-item"><a href="#">Vegetables</a></li> <li class="nav-item"><a href="#">Fruits</a></li> </ul> </nav> </div> 
      <div class="popular-product-section"> 
        <div class="popular-product-container"> <PopularProductComponent v-for="(product, index) in popularProducts" :key="index" :image="product.image" :name="product.name" :description="product.description" :productWeight="product.productWeight" :color="product.color" :originalPrice="product.originalPrice" :discountPrice="product.discountPrice" :rating="product.rating" /> </div> </div>
  </div>
  </div>

</template>

<script>
import CategoryComponent from './components/CategoryComponent.vue';
import ProductComponent from './components/ProductComponent.vue';
import PromotionComponent from './components/PromotionComponent.vue';
import PopularProductComponent from './components/PopularProductComponent.vue';

export default {
  name: 'App',
  components: {
    CategoryComponent,
    ProductComponent,
    PromotionComponent,
    PopularProductComponent
  },
  data() {
    return {
      categoryProducts: [
        { image: 'src/assets/burger.png', name: 'Cake & Milk', quantity: 14 , color: '#f6fbd8'},
        { image: 'src/assets/peach.png', name: 'Peach', quantity: 27 , color: '#d4c2ac'},
        { image: 'src/assets/kiwi.png', name: 'Organic Kiwi', quantity: 21, color: '#d6e3c3' },
        { image: 'src/assets/apple.png', name: 'Red Apple', quantity: 68, color: '#fec3c3' },
        { image: 'src/assets/snack.png', name: 'Snack', quantity: 34 , color: '#f6fbd8'},
        { image: 'src/assets/blackplum.png', name: 'Black Plum', quantity: 25, color: '##FFF3FF' },
        { image: 'src/assets/cabbage.png', name: 'Vegetables', quantity: 65 , color: '#F2FCE4'},
        { image: 'src/assets/Cake&milk.png', name: 'Cake & Milk', quantity: 33, color: '#F2FCE4' },
        { image: 'src/assets/headphone.png', name: 'Headphone', quantity: 54 , color: '#daeef5'},
        { image: 'src/assets/orange.png', name: 'Orange', quantity: 63 , color: '#feeac6'},
      ],
      promotionItems: [
        
        { image: 'src/assets/onine.png', text:'Everyday Fresh & Clean with Our Products', color: '#F0E8D5'},
        { image: 'src/assets/milk.png', text:'Make your breakfast fast Healthy and Easy', color: '#F3E8E8'},
        { image: 'src/assets/vet.png', text:'The best Organic Product Online', color: '#E7EAF3'},
      ],
      popularProducts: [ 
        { image: 'src/assets/mango.png', name: 'Hodo Foods', description:'Seeds of Change Organic Quinoa, Brown, & Red Rice', productWeight: 500, color: 'white', originalPrice: '$20', discountPrice: '$15', rating: '4.5' },
         { image: 'src/assets/corn.png', name: 'Hodo Foods', description:'All Natural Italian-Style Chicken Meatballs', productWeight: 500, color: 'white', originalPrice: '$30', discountPrice: '$25', rating: '4.0' },
         { image: 'src/assets/orangess.png', name: 'Hodo Foods',description:'Angie’s Boomchickapop Sweet & Salty Kettle Corn', productWeight: 500, color: 'white', originalPrice: '$30', discountPrice: '$25', rating: '4.0' },
          { image: 'src/assets/chili.png', name: 'Hodo Foods',description:'Foster Farms Takeout Crispy Classic Buffalo Wings', productWeight: 800, color: 'white', originalPrice: '$25', discountPrice: '$20', rating: '4.2' }, 
          { image: 'src/assets/lemon.png', name: 'Hodo Foods',description:'Blue Diamond Almonds Lightly Salted Vegetables', productWeight: 500, color: 'white', originalPrice: '$40', discountPrice: '$35', rating: '4.8' },
          { image: 'src/assets/mango.png', name: 'Hodo Foods', description:'Seeds of Change Organic Quinoa, Brown, & Red Rice', productWeight: 500, color: 'white', originalPrice: '$20', discountPrice: '$15', rating: '4.5' },
         { image: 'src/assets/corn.png', name: 'Hodo Foods', description:'All Natural Italian-Style Chicken Meatballs', productWeight: 500, color: 'white', originalPrice: '$30', discountPrice: '$25', rating: '4.0' },
         { image: 'src/assets/orangess.png', name: 'Hodo Foods',description:'Angie’s Boomchickapop Sweet & Salty Kettle Corn', productWeight: 500, color: 'white', originalPrice: '$30', discountPrice: '$25', rating: '4.0' },
          { image: 'src/assets/chili.png', name: 'Hodo Foods',description:'Foster Farms Takeout Crispy Classic Buffalo Wings', productWeight: 800, color: 'white', originalPrice: '$25', discountPrice: '$20', rating: '4.2' }, 
          { image: 'src/assets/lemon.png', name: 'Hodo Foods',description:'Blue Diamond Almonds Lightly Salted Vegetables', productWeight: 500, color: 'white', originalPrice: '$40', discountPrice: '$35', rating: '4.8' },
          
          
         ]
        
    };
  }
}
</script>

<style>
html, body { 
  background-color: white; 
  margin: 0; 
  padding: 0; 
  height: 100%; 
  width: 1856px; 
  margin-bottom: 20px;
  justify-content: center; 
  display: flex;/* Center the content horizontally */ 
  align-items: center;

} 
  
#app { 
  
  min-height: 100vh; 
  color: black;
  width: 1200px;
  margin: 0 auto;
  height: 100%;
 }
 header { 
  background-color: #f8f8f8; 
  padding: 10px 0; 
  display: flex; 
  justify-content: flex-end; /* Align header items to the right */ 
  width: 100%; 
  position: fixed;
  top:0;
  right: 0;
   } 
 .navbar { 
  display: flex; 
  justify-content: flex-end; 
  /* Align navbar items to the right */ 
  width: 100%;
  max-width: 1200px; 
   /* Match the main container width */  } 
 .nav-list { list-style: none; padding: 10; margin:10; display: flex; flex-wrap: nowrap; /* Ensure items stay in a single line */ /* Allow horizontal scrolling if needed */ } 
 .nav-item { margin: 0 15px; } .nav-item a { text-decoration: none; color: #333; font-weight: bold; font-size: 12px} .nav-item a:hover { color: #007bff; }
.main-container { 
  max-width: 1200px; 
  margin: 20px auto; 
  padding: 0;
  padding-top: 20px 0;
  
  
  
  }
.category-section, .promotion-section, .popular-product-section {
  margin: 20px 0;
  
}


.category-container , .promotion-container { display: flex; justify-content: center; /* Center the items */ flex-wrap: nowrap;}
.popular-product-container { display: flex; justify-content: center; /* Center the items */ flex-wrap: wrap; max-width: 1200px; }
.header-container { 
  display: flex; 
  justify-content: flex-end; /* Align headers horizontally */ 
  margin: 20px 0; 
  margin-right: -140px;
  }
  .popular-product-header { /* Set the font size for the Popular Product header */ white-space: nowrap; /* Prevent wrapping */ justify-content: flex-start;}
</style>