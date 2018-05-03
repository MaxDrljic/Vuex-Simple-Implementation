<template>
  <div id="app">
    <product-list-one></product-list-one>
    <product-list-two></product-list-two>
  </div>
</template>

<script>
import ProductListOne from './components/ProductListOne';
import ProductListTwo from './components/ProductListTwo';

export default {
  components: {
    ProductListOne,
    ProductListTwo
  },
  name: 'app',
  data () {
    return {
      
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Ubuntu');

body {
  font-family: Ubuntu;
  color: #555;
}
</style>
