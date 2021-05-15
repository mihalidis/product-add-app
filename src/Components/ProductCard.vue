<template>
  <div class="col-md-2 card">
    <img class="card-img-top" :src="product.selectedImage" alt="Card image cap">
    <div class="card-body">
      <h5 class="card-title">{{ product.name }}</h5>
      <small>
        <strong>Adet : </strong> {{ product.count }}
      </small>
      <br>
      <small>
        <strong>Fiyat : </strong> {{ product.price }}
      </small>
      <br>
      <small>
        <strong>Tutar : </strong> {{ product.price * product.count }}
      </small>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    product: Object
  }
}
</script>
<style>
.card{
  margin-right: 5px;
  margin-bottom: 5px;
}

.card:last-child{
  margin-right: 0;
}

.col-md-2{
  max-width: 15.666667%!important;
}
</style>