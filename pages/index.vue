<template>
  <div class="container">
    <div v-if="error">
      {{ error }}
    </div>
    <ul v-else>
      <li v-for="product in products" :key="product.id">
        {{ product.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      products: [],
      error: null
    }
  },
  async mounted () {
    try {
      this.products = await this.$strapi.$products.find()
    } catch (error) {
      this.error = error
    }
  }
}
</script>