<template>
  <div class="color-changer-container" :style="{ backgroundColor: selectedColor }">
    <h2>Box Color Changer</h2>
    <div class="button-container">
      <button @click="changeColor('white')" class="color-button">Putih</button>
      <button @click="changeColor('#006400')" class="color-button">Hijau Tua</button>
      <button @click="changeColor('#ADD8E6')" class="color-button">Biru Muda</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedColor: 'white', 
    };
  },
  methods: {
    changeColor(color) {
      this.selectedColor = color; 
    },
  },
};
</script>

<style scoped>
.color-changer-container {
  width: 100%;
  height: 200px; 
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 2px solid black;
  margin-top: 20px;
}

.button-container {
  margin-top: 10px;
  display: flex;
  gap: 10px; 
}

.color-button {
  padding: 10px 20px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  cursor: pointer;
  border-radius: 5px;
}

.color-button:hover {
  background-color: #ddd;
}
</style>