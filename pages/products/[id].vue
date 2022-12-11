<template>
    <div>Products {{ id }}</div>
    <p>Name: {{ product.title }}</p>
    <p>Price: {{ product.price }}</p>
</template>

<script setup>
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id
const { data: product } = await useFetch(uri, { key: id })
</script>

<style scoped></style>
