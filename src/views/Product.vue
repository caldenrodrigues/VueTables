<template lang="html">
  <div class="">
    <ProductID v-on:add-id="addID()"/>
    <ProductChain />
  </div>

</template>

<script>
import ProductChain from '../components/ProductChain.vue';
import ProductID from '../components/ProductID.vue'
export default {
  name: "Product",
  components: {
    ProductChain,
    ProductID,
  },
  methods: {
    addID() {
    }
  }
}
</script>

<style lang="css" scoped>
</style>
