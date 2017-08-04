<template>
    <div class="row content">      
      <div class="col-lg-6"> </div>
      <div class="col-lg-6">
        <cp-calculator></cp-calculator>
      </div>     
    </div>
</template>

<script>
import Calculator from './shared/calculator/Calculator.vue'
export default {
  name: 'home',
  data () {
    return {
      title: 'Home'
    }
  },
  components: {
    'cp-calculator': Calculator
  }
}
</script>

<style scoped>
  .content{padding: 25px 0 45px 0;}
</style>