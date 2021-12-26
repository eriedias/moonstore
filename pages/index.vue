<template>
  <section class="food-list">
    <div class="main-container">
      <div class="list">
        <div class="item">
          <figure>
            <img src="https://supermercadosrondon.com.br/guiadecarnes/images/postagens/quer_fazer_hamburger_artesanal_perfeito_2019-05-14.jpg">
          </figure>
          <div class="text">
            <h3>Nome da Comida</h3>
            <span class="price">$19</span>
          </div>
        </div>
        <div class="item">
          <figure>
            <img src="https://supermercadosrondon.com.br/guiadecarnes/images/postagens/quer_fazer_hamburger_artesanal_perfeito_2019-05-14.jpg">
          </figure>
          <div class="text">
            <h3>Nome da Comida</h3>
            <span class="price">$19</span>
          </div>
        </div>
        <div class="item">
          <figure>
            <img src="https://supermercadosrondon.com.br/guiadecarnes/images/postagens/quer_fazer_hamburger_artesanal_perfeito_2019-05-14.jpg">
          </figure>
          <div class="text">
            <h3>Nome da Comida</h3>
            <span class="price">$19</span>
          </div>
        </div>
      </div>
    </div>
    <button @click="increment()">
      Total: {{ total }}
    </button>
  </section>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  name: 'IndexPage',
  layout: 'DefaultHeader',
  computed: {
    total () {
      return this.$store.state.total
    }
  },
  methods: {
    ...mapMutations({
      increment: 'increment'
    })
  }
}
</script>
