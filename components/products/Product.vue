<template>
    <div>
        <div>
            <h1>
                <NuxtLink :to="`/products/${product.id}`">{{
                    product.title
                }}</NuxtLink>
            </h1>
            <div>{{ product.price }}</div>
            <div>{{ product.description }}</div>
            <div>{{ product.category }}</div>
            <div>{{ product.image }}</div>
        </div>
    </div>
</template>

<script setup>
import { inject } from 'vue'

const arr = inject('arr')
console.log(arr)

const { product } = defineProps({
    product: {
        type: Object,
        required: true,
    },
})
</script>

<style scoped></style>
