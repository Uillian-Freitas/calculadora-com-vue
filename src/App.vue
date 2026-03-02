<script setup>
import { reactive, onMounted, onBeforeUnmount } from 'vue';
import Display from './components/Display.vue'
import Botoes from './components/Botoes.vue'

const estado = reactive({
  valorAtual: '0',
  valorAnterior: null,
  operacao: null,
})

function lidarComClique(valor) {
  if (valor === 'C') {
    estado.valorAtual = '0'
    estado.valorAnterior = null
    estado.operacao = null
    return
  }

  if (['+', '-', '*', '/'].includes(valor)) {
    escolherOperacao(valor)
    return
  }

  if (valor === '=') {
    calcular()
    return
  }

  estado.valorAtual =
    estado.valorAtual === '0'
      ? valor
      : estado.valorAtual + valor
}

function escolherOperacao(op) {
  estado.valorAnterior = estado.valorAtual
  estado.operacao = op
  estado.valorAtual = '0'
}

function calcular() {
  const anterior = Number(estado.valorAnterior)
  const atual = Number(estado.valorAtual)
  let resultado = 0

  if (estado.operacao === '+') {
    resultado = anterior + atual
  }
  if (estado.operacao === '-') {
    resultado = anterior - atual
  }
  if (estado.operacao === '*') {
    resultado = anterior * atual
  }
  if (estado.operacao === '/') {
    resultado = anterior / atual
  }

  estado.valorAtual = String(resultado)
  estado.valorAnterior = null
  estado.operacao = null
}

function lidarComTeclado(event) {
  const tecla = event.key

  if (!isNaN(tecla)) {
    lidarComClique(tecla)
  }

  if (['+', '-', '*', '/'].includes(tecla)) {
    lidarComClique(tecla)
  }

  if (tecla === 'Enter') {
    lidarComClique('=')
  }

  if (tecla === 'Backspace') { 
    lidarComClique('C')
  }
}

onMounted(() => {
  window.addEventListener('keydown', lidarComTeclado)
})

onBeforeUnmount(() => {
  window.removeEventListener('keydown', lidarComTeclado)
})

</script>

<template>
  <div class="app">
  <div class="calculadora">
    <Display :valor="estado.valorAtual" />
    <Botoes @clicou="lidarComClique" />
  </div>
  </div>
</template>

<style scoped>
.app{
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #1f1f1f;
}

.calculadora {
  font-family:  Arial, sans-serif;
  width: 320px;
  border-radius: 20px;
  background: #1f1f1f;

  box-shadow: 
  8px 8px 18px #141414,
  -8px -8px 18px #2a2a2a;
}

</style>
