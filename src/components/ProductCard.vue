<template>
    <!-- component -->
    <div class="py-6 mx-4">
        <div class="flex max-w-md bg-white shadow-lg rounded-lg overflow-hidden">
            <div class="w-1/3 bg-cover" :style="{ backgroundImage: 'url(' + book.image + ')' }"></div>
            <div class="w-2/3 p-4">
                <h1 class="text-gray-900 font-bold text-2xl">{{ book.title.slice(0, 18) }}...</h1>
                <p class="mt-2 text-gray-600 text-sm">{{ book.description.slice(0, 95) }}...</p>
                <div class="flex item-center mt-2">
                    <svg class="w-5 h-5 fill-current text-gray-700" viewBox="0 0 24 24">
                        <path
                            d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z"
                        />
                    </svg>
                    <svg class="w-5 h-5 fill-current text-gray-700" viewBox="0 0 24 24">
                        <path
                            d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z"
                        />
                    </svg>
                    <svg class="w-5 h-5 fill-current text-gray-700" viewBox="0 0 24 24">
                        <path
                            d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z"
                        />
                    </svg>
                    <svg class="w-5 h-5 fill-current text-gray-500" viewBox="0 0 24 24">
                        <path
                            d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z"
                        />
                    </svg>
                    <svg class="w-5 h-5 fill-current text-gray-500" viewBox="0 0 24 24">
                        <path
                            d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z"
                        />
                    </svg>
                </div>
                <div class="flex item-center justify-between mt-3">
                    <h1 class="text-gray-700 font-bold text-xl">${{ book.price }}</h1>
                    <router-link
                        :to="{
                            name: 'Product',
                            params: { id: book.id },
                            props: { book }
                        }"
                        class="px-3 py-2 bg-gray-800 text-white text-xs font-bold uppercase rounded"
                        tag="button"
                    >More</router-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['book']
}
</script>

<style></style>
