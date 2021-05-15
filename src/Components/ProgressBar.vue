<template>
  <div class="progress">
    <div class="progress-bar bg-info" role="progressbar" :style="'width: '+ productList.length * 10 + '%'" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">
      {{ productList.length }}/10
    </div>
  </div>
</template>
<script>
import { eventBus } from "../main";
export default {
  data() {
    return {
      productList: [],
    }
  },
  created() {
    eventBus.$on("productList", list => {
      this.productList = list;
    });
  }
}
</script>
<style>
.progress {
  margin-bottom: 64px;
}
.progress-bar {
  color: black;
}

.bg-info {
  background-color: #da7f8f!important;
}
</style>