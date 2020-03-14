<template>
  <div>
      <ProductForm :funcReturn="onFormSubmit" />
      <ProductsList :products="products" />
  </div>
</template>

<script>
import ProductsList from './components/ProductsList.vue'
import ProductForm from './components/ProductForm.vue'

export default {
  name: 'App',
  components: {
    ProductsList,
    ProductForm
  },
  methods: {
    onFormSubmit(product) {
      this.products.push(product);
    }
  },
  data() {
    return {
      products: [
        {
          'name' : 'Assassins Creed Odyssey',
          'price' : '140.00',
          'urlImage' : 'https://images-americanas.b2w.io/produtos/01/00/item/133804/7/133804723_1GG.jpg',
          'description' : 'Assassin\'s Creed Odyssey coloca as escolhas do jogador em primeiro plano com várias inovações, à medida que você escolhe o herói que quer se tornar e muda o mundo à sua volta. Assuma o controle do seu destino a cada decisão que tomar e a cada relacionamento que formar. Personalize seu equipamento e domine habilidades especiais novas, ajustando o conjunto de habilidades do seu herói ao seu estilo de jogo. Lute em terras gregas, envolvendo-se em batalhas viscerais em terra e mar e tornando-se um verdadeiro herói lendário. Colocando suas escolhas no centro da experiência de jogo, Assassin\'s Creed Odyssey permite que você escreva sua própria odisseia.'
        },
        {
          'name' : 'Assassins Creed Origins',
          'price' : '120.00',
          'urlImage' : 'https://images-americanas.b2w.io/produtos/01/00/item/132594/9/132594963_1GG.jpg',
          'description' : 'Entre em uma jornada no Egito Antigo, o lugar mais misterioso de toda História, durante um período crucial que moldou o mundo que vivemos hoje. Descubra os segredos por trás das Grande Pirâmides, mitos esquecidos, os últimos faraós, e entalhada em hieróglifos perdidos no tempo - a história de origem da Irmandade dos Assassinos.'
        },
        {
          'name' : 'Assassins Creed Syndicate',
          'price' : '115.00',
          'urlImage' : 'https://images-americanas.b2w.io/produtos/01/00/item/132312/2/132312284_1GG.jpg',
          'description' : 'Londres, 1868! A Revolução Industrial. Uma era de invenções e prosperidade, erguida sobre o trabalho escravo da classe trabalhadora. Seja o gângster assassino Jacob Frye e recrute sua gangue para lutar por justiça em nome da classe trabalhadora oprimida. Lidere o submundo para retomar Londres, em uma aventura visceral repleta de ação, intriga e combates brutais. Apesar de ser o combustível do Império Britânico, os trabalhadores não passam de escravos legalizados que dão lucros para uma minoria. Vivendo na miséria e morrendo jovens, a classe baixa se une em protesto e formam um novo tipo de família, as gangues, que se voltam para uma vida no submundo, em sua luta para sobreviver. Até que os Assassinos chegam para reacender um conflito antigo envolvendo os líderes de Londres e que ecoará por toda a história moderna, desde o submundo até a classe mais alta.'
        },
        {
          'name' : 'Assassins Creed Iv: Black Flag',
          'price' : '50.00',
          'urlImage' : 'https://images-americanas.b2w.io/produtos/01/00/image/116923/5/116923552_1GG.jpg',
          'description' : 'Jogo de ação e aventura da série Assassin\'s Creed onde o capitão Edward Kenway, um pirata aterrorizante e assassino, ganha prestigio nos mares do Caribe, mas pode destruir tudo aquilo que os piratas já construíram.'
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
