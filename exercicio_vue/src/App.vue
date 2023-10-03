<script setup>

import calculos from './componentes'

export default {

  data() {
    return {
      num1: 0,
      num2: 0,
      operacao: null,
    }
  },
  calculos: {
    somar: function (num1, num2) {
      return num1 + num2;
    },
    diminuir: function (num1, num2) {
      return num1 - num2;
    },
    dividir: function (num1, num2) {
      return num1 / num2;
    },
    multiplicar: function (num1, num2) {
      return num1 * num2;
    },
  }

  computed : {
    resultado : { 
      this.calculaResultado(this.num1, this.num2, this.somar);
     },
     resultado : { 
      this.calculaResultado(this.num1, this.num2, this.diminuir);
     },
     resultado : { 
      this.calculaResultado(this.num1, this.num2, this.dividir);
     },
     resultado : { 
      this.calculaResultado(this.num1, this.num2, this.multiplicar);
     }
  }
}

</script>


<template>
  <div class="container">
    <header class="p-5 mb-4 mt-4 bg-light rounded-3">
      <h1>Calculadora de aritmética</h1>
    </header>
    <form>
      <div class="row">

        <div class="col">
              <input
              v-model="num1"  type="number" placeholder="Insira um número" required class="form-control" >
          </div>
          <div class="col">
              <input
              v-model="num1"  type="number" placeholder="Insira um número" required class="form-control" >
          </div>

        <div class="col-md-4">
            <select class="form-control" v-model="calculos">
                <option value="calculo">Selecionar Opções :</option>
                <option v-on:click="somar" value="soma">Soma</option>
                <option v-on:click="diminuir" value="subtracao">Subtração</option>
                <option v-on:click="dividir" value="divisao">Divisão</option>
                <option v-on:click="multiplicar" value="multiplicacao">multiplicação</option>
            </select>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
</style> 