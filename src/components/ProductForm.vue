<template>
    <div>
      <h1 class="title">Adicione um novo produto</h1>
      <form @submit="onFormSubmit">
        <div>
          <div class="column">
            <label>Nome</label>
            <input class="inputName" type="text" v-model="name">
          </div>
          <div class="column">
            <label>Preço (R$)</label>
            <input class="inputPrice" type="text" v-model="price">
          </div>
          <div class="column">
            <label>URL Imagem</label>
            <input class="inputUrlImage" type="text" v-model="urlImage">
          </div>
          <div class="column">
            <label>Descrição</label>
            <input class="inputDesc" type="text" v-model="description">
          </div>
        </div>
        <div class="divButton">
          <button class="button" type="submit">Adicionar</button>
        </div>
      </form>
    </div>
</template>

<script>
export default {
    name: 'ProductForm',
    props: {
        funcReturn: Function
    },
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

<style scoped>
.title{
    border-top: double;
    border-bottom: double;
    padding: 3px 5px;
    background: green;
    color: white;
}
.column {
  float: left;
}

.inputPrice {
  width: 100px;
}

.inputName {
  width: 200px;
}

.inputUrlImage {
  width: 550px;
}

.inputDesc {
  width: 800px;
}
.divButton {
  clear:both;
}
.button {
  background: green;
  color: white;
  margin: 15px 0px 30px 0px;
  padding: 5px;
  font-weight: bold;
}

label{
  font-weight: bold;
  margin: 1px;
  display:block;
}
input{
  margin: 1px 20px 10px 0px;
  display:block;
}
</style>