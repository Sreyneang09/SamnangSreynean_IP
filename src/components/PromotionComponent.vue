<template>
  <div class="promotion">
    <div class="promotion-item" v-for="(item, index) in items" :key="index " :style="{ backgroundColor: item.color }">
      <div class="promotion-content"> 
         
        <div class="promotion-text"> 
          <p>{{ item.text }}</p> 
          <ButtonComponent label="Shop Now" @click="handleButtonClick" /> </div> 
          <img :src="item.image" alt="Promotion Image">
        </div>
        
    </div>
  </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
  name: 'PromotionComponent',
  components: {
    ButtonComponent
  },
  props: {
    items: Array
  },
  methods: {
    handleButtonClick() {
      alert('Button clicked!');
    }
  }
}
</script>

<style scoped>
.promotion {
  display: flex;
  justify-content: space-around;
  flex-wrap: nowrap;
}
.promotion-item {
  background-color: #f5f5f5;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  margin: 10px;
  width: 450px;
  height: 250px;



  color: black;
}
.promotion-content { 
  display: flex; 
  align-items: center; 
  
} 
  .promotion-text { text-align: left; margin-right: 30px;  } 
  .promotion-text p { 
    margin-bottom: 30px;  
    margin-top: 40px;
    font-size: 20px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif
  }

  .promotion-content img { 
    width: 200px; 
    height: 200px; 
    margin-right: -20px;
    

     /* Space between image and text */ } 
  .promotion-text { text-align: left; }
</style>
