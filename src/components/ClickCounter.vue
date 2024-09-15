<template>
  <div class="counter-container">
    <h2>Click Counter</h2>
    <p>Current Count: {{ count }}</p>
    
    <!-- Tombol untuk menambah jumlah klik -->
    <button @click="increase" class="counter-tambah">+</button>
    
    <!-- Tombol untuk mengurangi jumlah klik -->
    <button @click="decrease" class="counter-kurang">-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0, 
    };
  },
  methods: {
    // Fungsi untuk menambah nilai count
    increase() {
      this.count++;
    },
    // Fungsi untuk mengurangi nilai count
    decrease() {
      if (this.count > 0) {
        this.count--;
      }
    },
  },
};
</script>

<style scoped>
.counter-container {
  text-align: center;
  margin-top: 20px;
}

.counter-tambah {
  padding: 10px 20px;
  background-color: #27d700;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin: 5px;
}
.counter-kurang {
  padding: 10px 20px;
  background-color: #ff0000;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin: 5px;
}

/* .counter-button:hover {
  background-color: #0056b3;
} */
</style>