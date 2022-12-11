<template>
    <div>Products</div>
    <div v-for="product in products" :key="product.id">
        <div>
            <NuxtLink :to="`/products/${product.id}`">{{
                product.title
            }}</NuxtLink>
        </div>
        <div>{{ product.price }}</div>
        <div>{{ product.description }}</div>
        <div>{{ product.category }}</div>
        <div>{{ product.image }}</div>
    </div>
</template>

<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped></style>
