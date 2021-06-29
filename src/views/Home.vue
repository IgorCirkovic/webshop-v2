<template>
  <div class="home">
    <ProductDescription 
      :product="product"
      :active="active.product_drawer"/>

    <div class="products-cards">
          <ProductSummary 
            v-for="product in products"
            :key="product.id"
            :product="product"
            v-on:view-product="viewProduct($event)"  />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import products from '../data/products.js'
import ProductSummary from '../components/products/ProductSummary.vue'
import ProductDescription from '../components/products/ProductDescription.vue'

export default {
  name: 'Home',
  components: {
    ProductSummary, ProductDescription
  },
  data (){
    return{
      products: products,
      product: null,
      active: {
        product_drawer: false
      }
    }
  },
  methods: {
    viewProduct(product){
      this.product = product
      console.log(this.product)
    }
  }
}
</script>

<style lang="css">
  .products-cards{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>