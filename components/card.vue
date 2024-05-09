<template>
    <div id="card" class="card">
        <img :src="imgURL", :alt="`product:${title}`" class="h-64 w-full object-cover" />
        <div class="p-3">
            <h4 class="font-bold text-lg">{{ title }}</h4>
            <span class="mt-1">{{ details }}</span>
        </div>
        <badget />
    </div>
</template>

<script setup lang="ts">
    const { imgURL, title, details} = defineProps<{
        imgURL:string,
        title:string,
        details:string
    }>()
</script>

<style scoped>

</style>