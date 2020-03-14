<template>
    <div>
      <h1>Novo Produto</h1>
      <form @submit="onFormSubmit">
        <p>
          <label>Nome:</label>
          <input type="text" v-model="name">
        </p>
        <p>
          <label>Descrição:</label>
          <input type="text" v-model="description">
        </p>
        <p>
          <label>Preço:</label>
          <input type="text" v-model="price">
        </p>
        <p>
          <label>URL Imagem:</label>
          <input type="text" v-model="urlImage">
        </p>
        <button type="submit">Adicionar</button>
      </form>
    </div>
</template>

<script>
export default {
    name: 'ProductForm',
    props: {
        funcReturn: Function
    },
    /*data() {
        return {
            name: '',
            price: 0.00,
            urlImage: '',
            description: ''
        }
    },*/
    methods: {
    onFormSubmit(e) {
      e.preventDefault();

      this.funcReturn({
        'name': this.name,
        'price': this.price,
        'urlImage': this.urlImage,
        'description': this.description
      });
    }
  }
}
</script>