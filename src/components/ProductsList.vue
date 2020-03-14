<template>
    <div>
        <ProductItem v-for="item in products" v-bind:key="item" v-bind:product="item" />
    </div>
</template>

<script>
import ProductItem from './ProductItem.vue'

export default {
    name: "products",
    components: {
      ProductItem
    },
    props: {
        products: Array
    }
}
</script>