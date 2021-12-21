<template>
  <div>
    <app-stock v-for="(stock, indexOfStock) in stocks" :key="indexOfStock" :stock="stock"></app-stock>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex';
  import Stock from './Stock.vue';

  export default {
    computed: {
      ...mapGetters({
        stocks: 'stockPortfolio',
      })
    },
    components: {
      appStock: Stock,
    }
  }
</script>

<style></style>