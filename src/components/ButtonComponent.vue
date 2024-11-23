<template>
  <button @click="handleClick" :style="{ backgroundColor: color }" class="shop-button">
    {{ label }} <span class="arrow">→</span>
  </button>
</template>

<script>
export default {
  name: 'ButtonComponent',
  props: {
    label: String,
    color: String
  },
  methods: {
    handleClick() {
      this.$emit('click');
    }
  }
}
</script>

<style scoped>
.shop-button {
  color: rgb(254, 255, 254);
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 5px;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  transition: background-color 0.3s ease;
  background: rgb(55, 147, 76);
}
.shop-button:hover {
  filter: brightness(0.9);
  background: rgb(234, 59, 94);
}
.arrow {
  margin-left: 10px;
  font-size: 18px;
}
</style>
