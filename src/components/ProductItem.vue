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
    /*data(){
        return {
            name: '',
            price: 0.00,
            urlImage: '',
            description: ''
        }
    },
    computed: {
        item : {
            // getter
            get: function() {
                return {
                    'name' : this.name,
                    'price' : this.price,
                    'urlImage' : this.urlImage,
                    'description' : this.description
                }
            },
            set: function(newItem) {
                if(newItem != null){
                    if(newItem.hasOwnProperty('name'))
                        this.name = newItem['name'];
                    if(newItem.hasOwnProperty('price'))
                        this.price = newItem['price'];
                    if(newItem.hasOwnProperty('urlImage'))
                        this.urlImage = newItem['urlImage'];
                    if(newItem.hasOwnProperty('description'))
                        this.description = newItem['description'];
                }
            }
        }
    }*/
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
