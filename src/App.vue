<template>
  <div class="container">
    <navbar/>
    <add-product/>
    <progress-bar/>
    <list-products/>
  </div>


</template>

<script>
import addProduct from "./Components/AddProduct";
import progressBar from "./Components/ProgressBar.vue";
import listProducts from "./Components/ListProducts.vue";
import navbar from "./Components/Layout/Navbar.vue";
  export default {
    components: {
      addProduct,
      progressBar,
      listProducts,
      navbar
    }
  }
</script>

<style>
  body {
    background-color: #faf3f3;
    padding-top: 20px;
    padding-bottom: 20px;
  }
</style>

