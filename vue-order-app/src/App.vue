<template>
  <div>
    <h1>Order Your Items</h1>
    <OrderCounter />
  </div>
</template>

<script>
import OrderCounter from './components/OrderCounter.vue';

export default {
  components: {
    OrderCounter
  }
};
</script>

<style>
h1 {
  text-align: center;
}
</style>

