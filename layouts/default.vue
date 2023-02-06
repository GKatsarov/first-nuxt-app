<template>
    <div class="min-h-full">
        <Navbar />
        <slot></slot>
    </div>
</template>
<script setup>
useHead({
    htmlAttrs: { class: 'h-full bg-gray-50' },
    bodyAttrs: { class: 'h-full' },
})
</script>
създавам проект на vit/ + module tailwind css + stigma landing page/single design + 