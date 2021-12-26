<template>
  <section class="food-list">
    <div class="main-container">
      <div class="list">
        <div v-for="(product, index) in products" :key="index" class="item">
          <figure>
            <img :src="product.image">
          </figure>
          <div class="text">
            <h3>{{ product.title }}</h3>
            <span class="price">$ {{ product.price }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { mapMutations, mapState } from 'vuex'

export default {
  name: 'IndexPage',
  layout: 'DefaultHeader',
  async fetch () {
    this.setProducts(await fetch(
      'https://fakestoreapi.com/products'
    ).then(res => res.json()))
  },
  computed: {
    ...mapState([
      'products'
    ])
  },
  methods: {
    ...mapMutations({
      setProducts: 'setProducts'
    })
  }
}
</script>
