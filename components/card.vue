<template>
    <div id="card" class="card text-center">
        <img :src="product.image" :alt="`product:${product.title}`" class="h-64 object-cover mx-auto my-auto p-8" />
        <div class="p-3">
            <h4 class="font-bold text-lg one-line">{{ product.title.slice(0, 40) + '...' }}</h4>
            <span class="truncate">{{ product.description.slice(0, 40) + '...' }}</span>
            <NuxtLink :to="`/food/${product.id}`" class="btn-active my-3">View Details</NuxtLink>
        </div>
        <badget />
    </div>
</template>

<script setup lang="ts">
import type { IFood } from '~/interface/IFood';
    const props = defineProps<{
        product: IFood
    }>()
</script>

<style scoped>

</style>