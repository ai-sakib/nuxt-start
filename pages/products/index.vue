<template>
    <div>Products</div>
    <div v-for="product in products" :key="product.id">
        <Product :product="product" />
    </div>
</template>

<script setup>
import Product from '~~/components/products/Product.vue'

const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped></style>
