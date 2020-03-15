<template>
    <div>
        <h1 class="title">Lista de Produtos (Quantidade: {{quant}})</h1>
        <ProductItem class="product" v-for="item in products" :key="item" :product="item" />
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
        products: Array,
        quant: String
    }
}
</script>

<style scoped>
.title{
    border-top: double;
    border-bottom: double;
    padding: 3px 5px;
    background: green;
    color: white;
}
.product{
    float: left;
    clear:both;
    border-bottom: double;
    margin-bottom: 5px;
    padding-bottom: 15px;
}
</style>
