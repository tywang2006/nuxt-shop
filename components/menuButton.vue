<template>
    <li class="py-1">
        <NuxtLink :to="to" :class="`px-4 flex justify-end border-r-4 ${selectClass}`">
            <span>{{ title }}</span>
            <slot />
        </NuxtLink>
    </li>
</template>

<script setup lang="ts">
    const { title, to } = defineProps<{
        'title':string,
        'to':string
    }>()
    const route = useRoute()

    const selectClass = computed(()=>{
        let name:any = route.name==='index'?'home':route.name
        let isSelected = name.includes(title.toLowerCase())
        return isSelected?"border-primary font-bold":""
    })

    console.log(route.name)
</script>

<style scoped>

</style>