<template>
  <div class="home">
    <div class="splash-container">
        <div class="splash">
          <h1>Splendid Food</h1>
        </div>
      </div>

      <main class="wrapper">

        <h2>Recommended</h2>

        <div class="recommended">

          <ProductCart v-for="(product,index) in inventory.slice(0,3)"
          :key="product.id"
          :index="index"
          :product="product"
          :addToCart="addToCart"
          class="card">
          </ProductCart>

        </div>

      </main>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductCart from '@/components/ProductCart.vue'

export default {
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCart
  }
}
</script>
