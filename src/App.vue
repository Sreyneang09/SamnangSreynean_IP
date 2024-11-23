<template>
  <div id="app">
    
     <div class="main-container">
      <p>This is my first Vue.js </p>
       <div class="category-section"> <h> Category Component</h> 
         <div class="category-container"> <CategoryComponent v-for="(product, index) in categoryProducts" :key="index" :image="product.image" :name="product.name" :quantity="product.quantity" :color="product.color" /> </div>
         </div >
       <div class="promotion-section">
       <h>Promotion Component</h>
       <div class="promotion-container"> <PromotionComponent :items="promotionItems" />
       </div>
    </div>
  </div>
  </div>

</template>

<script>
import CategoryComponent from './components/CategoryComponent.vue';
import ProductComponent from './components/ProductComponent.vue';
import PromotionComponent from './components/PromotionComponent.vue';
export default {
  name: 'App',
  components: {
    CategoryComponent,
    ProductComponent,
    PromotionComponent
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
      ]
    };
  }
}
</script>

<style>

.main-container { 
  max-width: 1200px; 
  margin: 0 auto; 
  padding: 10px; }
.category-section, .promotion-section {
  margin: 20px;
  margin-right: 20px;
}
.category-container { display: flex; justify-content: space-around;flex-wrap: nowrap; }
.promotion-container { display: flex; justify-content: space-around;flex-wrap: nowrap; }
</style>
