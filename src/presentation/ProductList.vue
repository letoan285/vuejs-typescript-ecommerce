<template>
  <div id="product-app">
      <h2>{{getName('PRoduct App')}}</h2>
      <button @click="changeName('New Name')">Change Name</button>
  </div>
</template>

<style lang="scss">

</style>
<script lang="ts">
import Vue from 'vue';
interface IData {}
export default Vue.extend({
  components: {
    
  },
  data(){
    return {
      name: 'Product List'
    }
  },
  created(){
    this.name = 'Product Created'
  },
  mounted(){
    this.name = 'Product Detail'
  },
  methods: {
    getName(name: string){
      this.name = name;
      return this.name;
    },
    changeName(name: string){
      this.$emit('changeMyName');
    }
  }
})
</script>
