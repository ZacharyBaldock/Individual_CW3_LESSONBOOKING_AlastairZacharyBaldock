<template>
<div>
    <h2>Checkout</h2>
    <h3>Added products</h3>
    <div v-for='product in cart' :key="product.id">
        {{product.id}} 
        <button @click="cart.splice(index,1)">remove</button>
    </div>
    <p>
        <strong> Name </strong>
        <input v-model="name" />
        <strong> Address </strong>
        <input v-model="address" /> <button>Submit</button>
    </p>
</div>
</template>

<script>
export default {
    name: "Form",
    props: ['cart'],
    data() {
        return {
        name: "",
        address: "",
        };
    },
    
};
</script>