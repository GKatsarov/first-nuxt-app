<template>
    <h1 class="text-3xl font-bold underline">
        I am iphone {{ name }}
    </h1>
</template>

<script setup>

const name = computed(()=>{
    return useRoute().params.name.replaceAll('-', ' ');
})
</script>