<template>
    <router-link
        to="/cart"
        v-if="showCartButton"
        class="floating-button bg-blue-300 hover:bg-blue-700 shadow-lg"
        tag="button"
    >
        <h2>{{ cart.length }}</h2>
        <img src="../assets/shopping-cart-svgrepo-com.svg" alt="cart image"
    /></router-link>
</template>

<script>
export default {
    computed: {
        cart() {
            return this.$store.getters.getCart
        },
        showCartButton() {
            if (this.cart.length >= 1) {
                return true
            } else {
                return false
            }
        }
    }
}
</script>

<style lang="scss">
.floating-button {
    position: fixed;
    right: 10px;
    top: 10px;
    border-radius: 100% !important;
    height: 60px;
    width: 60px;
    display: flex;
    justify-content: center;
    align-items: center;

    img {
        height: 20px;
        width: 20px;
        margin-left: 4px;
    }
}
</style>
