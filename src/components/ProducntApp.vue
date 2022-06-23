<template>
<div>
    <h1>Products</h1>
    <div class="products">
        <div v-for="(item, index) in products" :key="index">
          <h3>{{item.name}}</h3>
          <img :src="item.image" />
          <div>{{item.cost}}</div>
          <button @click="addItemCartComponent(item)">Add to cart</button>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'ProductApp',
    data() {
        return {
            products: [
                {
                name: "Produc1",
                cost: "100",
                image: "https://cdn-images.threadless.com/threadless-media/artist_shops/shops/vue/products/195803/shirt-1490421379-02ee987be67c75475b5b71a704b54987.png?v=3&d=eyJvbmx5X21ldGEiOiBmYWxzZSwgImZvcmNlIjogZmFsc2UsICJvcHMiOiBbWyJ0cmltc2NyaXB0IiwgWzEyMDAuMCwgMTM3MS40Mjg1NzE0Mjg1NzEzXSwge31dLCBbImVuY29kZSIsIFsiLnBuZyJdLCB7ImRwaSI6IDMwMH1dLCBbInJlc2l6ZSIsIFs4NThdLCB7fV0sIFsib3ZlcmxheSIsIFsidGhyZWFkbGVzcy1tZWRpYS9hcnRpc3Rfc2hvcHMvb3ZlcmxheXMvY2F0ZWdvcmllcy9tZW5zL3NpemVzLyovc3R5bGVzL3RyaWJsZW5kLXRlZS9jb2xvcnMvKi9mcm9udC5wbmciXSwgeyJ5IjogNDcwLCAieCI6IDU1OSwgImJhY2tncm91bmQiOiAiZjBmMGYyIn1dLCBbInJlc2l6ZSIsIFsxNTBdLCB7fV0sIFsiY2FudmFzX2NlbnRlcmVkIiwgWzE1MCwgMTUwLCAiI2ZmZmZmZiJdLCB7fV0sIFsiZW5jb2RlIiwgWyJqcGciLCA4NV0sIHt9XV19"
                },
                {
                name: "Produc2",
                cost: "200",
                image: "https://cdn-images.threadless.com/threadless-media/artist_shops/shops/vue/products/195803/shirt-1490421379-02ee987be67c75475b5b71a704b54987.png?v=3&d=eyJvbmx5X21ldGEiOiBmYWxzZSwgImZvcmNlIjogZmFsc2UsICJvcHMiOiBbWyJ0cmltc2NyaXB0IiwgWzEyMDAuMCwgMTM3MS40Mjg1NzE0Mjg1NzEzXSwge31dLCBbImVuY29kZSIsIFsiLnBuZyJdLCB7ImRwaSI6IDMwMH1dLCBbInJlc2l6ZSIsIFs4NThdLCB7fV0sIFsib3ZlcmxheSIsIFsidGhyZWFkbGVzcy1tZWRpYS9hcnRpc3Rfc2hvcHMvb3ZlcmxheXMvY2F0ZWdvcmllcy9tZW5zL3NpemVzLyovc3R5bGVzL3RyaWJsZW5kLXRlZS9jb2xvcnMvKi9mcm9udC5wbmciXSwgeyJ5IjogNDcwLCAieCI6IDU1OSwgImJhY2tncm91bmQiOiAiMTgxODE4In1dLCBbInJlc2l6ZSIsIFsxNTBdLCB7fV0sIFsiY2FudmFzX2NlbnRlcmVkIiwgWzE1MCwgMTUwLCAiI2ZmZmZmZiJdLCB7fV0sIFsiZW5jb2RlIiwgWyJqcGciLCA4NV0sIHt9XV19"
                },
                {
                name: "Produc3",
                cost: "300",
                image: "https://cdn-images.threadless.com/threadless-media/artist_shops/shops/vue/products/195795/shirt-1490420206-a15bc00a09077730c2a8dd98907d1b10.png?v=3&d=eyJvbmx5X21ldGEiOiBmYWxzZSwgImZvcmNlIjogZmFsc2UsICJvcHMiOiBbWyJ0cmltc2NyaXB0IiwgWzEyMDAuMCwgMTM3MS40Mjg1NzE0Mjg1NzEzXSwge31dLCBbImVuY29kZSIsIFsiLnBuZyJdLCB7ImRwaSI6IDMwMH1dLCBbInJlc2l6ZSIsIFs4NThdLCB7fV0sIFsib3ZlcmxheSIsIFsidGhyZWFkbGVzcy1tZWRpYS9hcnRpc3Rfc2hvcHMvb3ZlcmxheXMvY2F0ZWdvcmllcy9tZW5zL3NpemVzLyovc3R5bGVzL3RyaWJsZW5kLXRlZS9jb2xvcnMvKi9mcm9udC5wbmciXSwgeyJ5IjogNDcwLCAieCI6IDU1OSwgImJhY2tncm91bmQiOiAiN2M3YzdjIn1dLCBbInJlc2l6ZSIsIFsxNTBdLCB7fV0sIFsiY2FudmFzX2NlbnRlcmVkIiwgWzE1MCwgMTUwLCAiI2ZmZmZmZiJdLCB7fV0sIFsiZW5jb2RlIiwgWyJqcGciLCA4NV0sIHt9XV19"
                }
            ]
        }
    },
    methods: {
        addItemCartComponent(event){
            this.$emit("addItemCartForwardRcv", event);
        }
    }
}
</script>

<style>

</style>