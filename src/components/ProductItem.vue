<template>
    <div>
        <p class="title">{{product.name}}</p>
        <img class="image" v-bind:src="product.urlImage" />
        <p class="price">R$ {{product.price}}</p>
        <p class="desc">{{product.description}}</p>
    </div>
</template>

<script>
export default {
    name: "product",
    props: {
        product: Object
    }
};
</script>

<style scoped>
.title{
    font-size: 26px;
    font-weight: bold;
}
.image {
    height: 250px;
    width: 220px;
    float: left;
}
.price{
    font-size: 20px;
    font-weight: bold;
}
.desc{
    text-align: justify;
    text-justify: inter-word;
}
</style>
