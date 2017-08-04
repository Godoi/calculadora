<template>
  <div>
    <h3> Calculadora </h3>
    <div class="calculator"> 

      {{ operacao }} = {{ result }}
      <input type="text" class="form-control screen" value="" aria-label="...">

      <div class="keyboard btn-group" role="group" aria-label="...">
        <div class="keys">
          <button type="button" class="btn btn-default btn-number" @click="setEquacao(7)"> 7 </button>
          <button type="button" class="btn btn-default btn-number" @click="setEquacao(8)"> 8 </button>
          <button type="button" class="btn btn-default btn-number" @click="setEquacao(9)"> 9 </button>
          <button type="button" class="btn btn-default btn-operator" @click="setEquacao('/')"> ÷ </button>
        </div>
        <div class="keys">
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(4)"> 4 </button>
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(5)"> 5 </button>
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(6)"> 6 </button>
          <button type="button" class="btn btn-default btn-operator" v-on:click="setEquacao('*')"> X </button>
        </div>
        <div class="keys">
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(1)"> 1 </button>
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(2)"> 2 </button>
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(3)"> 3 </button>
          <button type="button" class="btn btn-default btn-operator" v-on:click="setEquacao('-')"> - </button>
        </div>
        <div class="keys">
          <button type="button" class="btn btn-default btn-number" v-on:click="setEquacao(0)"> 0 </button>
          <button type="button" class="btn btn-default btn-operator" v-on:click="setEquacao('.')"> . </button>
          <button type="button" class="btn btn-default btn-equal" v-on:click="getResultado('=')"> = </button>
          <button type="button" class="btn btn-default btn-operator" v-on:click="setEquacao('+')"> + </button>
        </div>
      </div>
            
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        result: '',
        operacao: ''
      }
    },
    methods: {
      setEquacao (content) {
        this.operacao += content
      },
      getResultado () {
        this.result = this.operacao
      },
      setSubtracao (num1, num2) {
        if (!isNaN(num1) && !isNaN(num2)) {
          this.result = num1 - num2
        }
      },
      setAdicao (num1, num2) {
        if (!isNaN(num1) && !isNaN(num2)) {
          this.result = num1 + num2
        }
      },
      setMultiplicacao (num1, num2) {
        if (!isNaN(num1) && !isNaN(num2)) {
          this.result = num1 * num2
        }
      }
    }
  }
</script>

<style lang="sass">
  @import './Calculator.scss';
</style>