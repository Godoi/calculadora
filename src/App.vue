<template>
  
  <div>
    <cp-header/>
      <transition name="pagina">
        <div class="container">
          <router-view></router-view>
        </div>
      </transition>
    <cp-footer/>
  </div>
  
</template>

<script>
import Header from './components/shared/header/Header.vue'
import Footer from './components/shared/footer/Footer.vue'

export default {
  name: 'app',
  components: {
    'cp-header': Header,
    'cp-footer': Footer
  }
}
</script>

<style>
  body {
    font-family: 'Open Sans', Arial, Helvetica, sans serif;
    font-size: 14px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    margin-top: 60px;
  }
  .page-enter, .page-leave-active {opacity: 0;}
  .page-enter-active, .page-leave-active {transition: opacity .4s;}
</style>
