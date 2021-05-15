<template>
  <div class="product-list">
    <h3 class="text-center">Eklenen Ürünlerin Listesi</h3>
    <div class="row product-container" >
      <product-card v-for="product in productList" :product="product"/>
    </div>
  </div>
</template>
<script>
import productCard from "./ProductCard";
import { eventBus } from "../main";
export default {
  components: {
    productCard
  },
  data() {
    return {
      productList: [],
    }
  },
  created() {
    eventBus.$on("product", item => {
      if(this.productList.length < 10){
        this.productList.push(item);
      }else {
        alert("Max ürün limitine ulaştınız!");
      }
    });

    eventBus.$emit("productList", this.productList);
  }
}
</script>
<style scoped>
  .product-container{
    margin-left: 15px;
  }
</style>