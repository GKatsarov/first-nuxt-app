<template>
    <div v-if="pending">
        Loading ...
    </div>
    <div v-else>
        <div class="bg-white">
            <div class="mx-auto max-w-2xl px-4 sm:px-6 lg:max-w-7xl lg:px-8">

            <div class="mt-6 grid grid-cols-1 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
                <div v-for="post in posts" :key="post.id" class="group relative">
                <div class="min-h-80 aspect-w-1 aspect-h-1 w-full overflow-hidden rounded-md bg-gray-200 group-hover:opacity-75 lg:aspect-none lg:h-80">
                    <img :src="post.image" :alt="post.imageAlt" class="h-full w-full object-cover object-center lg:h-full lg:w-full" />
                </div>
                <div class="mt-4 flex justify-between">
                    <div>
                    <h3 class="text-sm text-gray-700">
                        <a :href="`catalog/${post.slug}`">
                        <span aria-hidden="true" class="absolute inset-0" />
                        {{ post.title }}
                        </a>
                    </h3>
                    <p class="mt-1 text-sm text-gray-500">{{ post.description }}</p>
                    </div>
                    <p class="text-sm font-medium text-gray-900">{{ post.continent }}</p>
                </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script setup>
const { pending, data: posts } = useLazyFetch('https://api.nuxtjs.dev/posts');
</script>