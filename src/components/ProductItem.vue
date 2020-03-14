<template>
    <div>
        <h3>{{product.name}}</h3>
        <img v-bind:src="product.urlImage" />
        <h4>R$ {{product.price}}</h4>
        <h5>{{product.description}}</h5>
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