<template>
<div>
    <h1>Your Cart</h1>
    <div class="products">
        <div v-for="(cartitem, index) in cart" :key="index">          
          <h3>{{index}} - {{cartitem.name}}</h3>
          <img :src="cartitem.image" />
          <div>{{cartitem.cost}}</div>
          <button @click="removeItemFromCart(index)">Remove from cart</button>
        </div>
    </div>
</div>
</template>

<script>

export default{
   name: 'CartApp',
   props : ['cart'],
   methods: {
    removeItemFromCart(event){
        // console.log(event);
        this.$emit("removeItemFromCartForwRec", event);
    }
   }
}
</script>

<style>

</style>
