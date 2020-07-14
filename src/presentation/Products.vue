<template>
  <div id="product-app">
     <ProductList :changeMyName="changeName"/>
  </div>
</template>

<style lang="scss">
#product-app {
    min-height: 300px;
}
</style>
<script lang="ts">
import ProductList from './ProductList.vue';
interface IData {}
export default {
      components: {
    ProductList
  },
    methods: {
        changeName(){
            alert('new name')
        }
    }

}
</script>
