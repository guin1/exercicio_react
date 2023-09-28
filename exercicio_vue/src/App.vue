<script setup>

    somar() {
      this.operador = (num1, num2) => num1 + num2;
      this.setarValor();
    },
    diminuir() {
      this.operador = (num1, num2) => num1 - num2;
      this.setarValor();
    },
  dividir() {
      this.operador = (num1, num2) => num1 / num2;
      this.setarValor();
    },
    multiplicar() {
      this.operador = (num1, num2) => num1 * num2;
      this.setarValor();
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
              <input>
                  type="number" placeholder="Insira um número" required class="form-control">
          </div>
          <div class="col">
              <input
                  type="number" placeholder="Insira um número" required class="form-control">
          </div>
        <div class="col-md-4">
            <select class="form-control">
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