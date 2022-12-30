<template>
  <div class="dd">
    <img  src="../public/img/header-cart.svg" width="30" height="34" alt="1">
      <use xlink:href="#cart-icon"></use>
  <text class="cart-counter">{{ counter }}</text>
  </div>
<!--  <button @click="incrementCounter">Add to cart</button>-->
</template>

<script>
export default {
  name: 'CartIcon',
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    incrementCounter() {
      this.counter += 1;
    },
  },
};
</script>

<style>

</style>

