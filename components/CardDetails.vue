<template>
    <Head>
        <Title>{{ details.title }}</Title>
        <Meta name="description" :content="details.title" />
    </Head>
    <div class="card grid grid-cols-2 gap-10">
        <img class="mx-auto my-7" :src="details.image" :alt="`Product:${details.id}is not loaded`">
        <div class="p-7 flex flex-col justify-between">
            <div>
                <h2 class="text-4xl my-7">{{ details.title }}</h2>
                <p class="text-xl my-7">Price - ${{ details.price }}</p>
                <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
                <p class="mb-7">{{ details.description }}</p>
            </div>
            <button class="btn-active">
                <i class="mr-2">Add to cart</i>
            </button>
        </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import type { IFood } from '~/interface/IFood';
  
  const { id } = defineProps(['id'])
  const { data: product } = await useFetch('https://fakestoreapi.com/products/' + id)
  const details: IFood = <IFood>product.value
  
  </script>
  
  <style scoped>
    .card {
      position: relative; /* Required for positioning */
    }
  
    .back-home {
      margin-right: 10px;
      margin-bottom: 20px;
    }
  </style>
  