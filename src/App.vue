<template>
<div>
  <header>
    <button @click="navigateTo('products')">view product</button>
    {{ cart.length }} in cart 
    <button @click="navigateTo('cart')">view cart</button>
  </header>

  <div v-if="page === 'cart'">
    <CartApp :cart="cart" @removeItemFromCartForwRec="removeItemFromCart" />
  </div>

 <div v-if="page === 'products'">
    <ProdunctApp @addItemCartForwardRcv="addItemCartNew" />
  </div>

</div>
</template>

<script>
import ProdunctApp from "./components/ProducntApp.vue";
import CartApp from "./components/CartApp.vue";

export default {
  name: 'App',
  data() {
    return {
      cart: [],
      page: "products",
    }
  },
  components: {ProdunctApp, CartApp},
  methods: {
    addItemCartNew(event) {
      // console.log(event);
      this.cart.push(event);
      // console.log(this.cart);
    },
    navigateTo(event) {
      this.page = event;
    },
    removeItemFromCart(event) {
      //  console.log(event);
       this.cart.splice(event, 1);
    }
  }
  
}
</script>
<style>
body {
  margin: 0;
  padding: 3px;
}
.products{
  display: grid;
  grid-template-columns: 260px 260px 260px;
}
</style>
<style scoped>

header {
  height:60px;
  background-color: #eee;
  box-shadow: 2px 2px 5px #999;
  text-align: right;
  font-size: 30px;
  padding-top: 20px;
}
</style>
