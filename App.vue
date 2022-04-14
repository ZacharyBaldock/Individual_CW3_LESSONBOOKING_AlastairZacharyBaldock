<template>
<div id="app">
    <header>
        <h1>{{Classbooking}}</h1>
        <button @click="showCheckout">{{ this.cart.length }}Checkout</button>
    </header>
    <main> 
      <product-list @addProduct='addToCart'></product-list>
      
    <checkout :cart='cart'></checkout>  
    </main>
</div>
</template>

<script>
import ProductList from "./components/ProductList.vue";
import checkout from "./componenets/Form.vue";

export default {
    name: "App",
    components: {
     ProductList,
     checkout,
    },
    data() {
        return {
        sitename: "Vue.js Class booking",
        cart: [],    
        };  
    }, 
    methods: { 
      showCheckout() {},
      addToCart(product) {
        console.log("addProduct event received by the root component");
        this.cart.push(product);
      },
    },
  };
  </script>