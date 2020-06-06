<template>
    <div class="flex justify-center bg-white h-screen">
        <div class="flex flex-col w-full p-8 text-gray-800 pin-r pin-y md:w-4/5 lg:w-4/5">
            <h1 class="text-4xl">Your cart</h1>

            <div class="flex-1">
                <table class="w-full text-sm lg:text-base" cellspacing="0">
                    <thead>
                        <tr class="h-12 uppercase">
                            <th class="hidden md:table-cell text-left"></th>
                            <th class="text-left">Product</th>
                            <th class="lg:text-right text-left pl-5 lg:pl-0">
                                <span class="lg:hidden" title="Quantity">Qtd</span>
                                <span class="hidden lg:inline">Quantity</span>
                            </th>
                            <th class="hidden text-right md:table-cell">Unit price</th>
                            <th class="text-right">Total price</th>
                        </tr>
                    </thead>
                    <tbody class="text-left">
                        <tr v-for="(item, index) in books" :key="index">
                            <td class="hidden pb-4 md:table-cell">
                                <a href="#">
                                    <img :src="item.image" class="w-20 rounded" alt="Thumbnail" />
                                </a>
                            </td>
                            <td>
                                <a href="#">
                                    <p class="mb-2 md:ml-4">{{ item.title }}</p>
                                    <form action method="POST">
                                        <button type="submit" class="text-gray-700 md:ml-4">
                                            <small>(Remove item)</small>
                                        </button>
                                    </form>
                                </a>
                            </td>
                            <td>
                                <div class="w-20 float-right flex">
                                    <input
                                        type="text"
                                        v-model="item.counter"
                                        class="w-full font-semibold text-center text-gray-700 bg-gray-200 outline-none focus:outline-none hover:text-black focus:text-black"
                                    />
                                </div>
                            </td>
                            <td class="hidden text-right md:table-cell">
                                <span class="text-sm lg:text-base font-medium">${{ item.price }}</span>
                            </td>
                            <td class="text-right">
                                <span
                                    class="text-sm lg:text-base font-medium"
                                >${{ item.price * item.counter }}</span>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {}
    },
    computed: {
        cart() {
            return this.$store.getters.getCart
        },
        books() {
            return this.cart
        }
    },
    methods: {}
}
</script>

<style></style>
