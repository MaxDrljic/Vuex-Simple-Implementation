<template>
  <div id="product-list-one">
    <h2>Product List One</h2>
    <ul>
      <li v-bind:key="product" v-for="product in saleProducts">
        <span class="name">{{product.name}}</span>
        <span class="price">${{product.price}}</span>
      </li>
    </ul>
    <button v-on:click="reducePrice(4)">Reduce Price</button>
  </div>
</template>

<script>
import {mapActions} from 'vuex';
import {mapGetters} from 'vuex';

export default {
  computed: {
    // Accessing the State Products
    products() {
      return this.$store.state.products;
    },
    // Basic implementation of Getter & mapGetters
    ...mapGetters([
      'saleProducts'
    ])
  },
  methods: {
    // Basic implementation of Mutation & mapActions
    ...mapActions([
      'reducePrice'
    ])
  }
}
</script>

<style scoped>
#product-list-one {
  background: #FFF8B1;
  box-shadow: 1px 2px 3px rbga(0,0,0,0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}

#product-list-one ul {
  padding: 0;
}

#product-list-one li {
  display: inline-block;
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255,255,255,0.7);
}

.price {
  font-weight: bold;
  color: #E8800C;
}
</style>
