<template>
  <div class="order-container">
    <div v-for="(item, index) in items" :key="index" class="order-item">
      <span>{{ item.name }}</span>
      <button @click="decrease(index)">-</button>
      <span>{{ item.count }}</span>
      <button @click="increase(index)">+</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: "Eggs", count: 2 },
        { name: "Tortillas", count: 0 },
        { name: "Chocolate", count: 100 },
      ],
    };
  },
  methods: {
    increase(index) {
      this.items[index].count++;
    },
    decrease(index) {
      if (this.items[index].count > 0) {
        this.items[index].count--;
      }
    },
  },
};
</script>

<style scoped>
.order-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 200px;
}
.order-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
}
button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
  border-radius: 3px;
}
button:hover {
  background-color: #0056b3;
}
</style>
