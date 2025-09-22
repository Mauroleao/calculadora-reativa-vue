<script setup>
  import { reactive, computed } from 'vue'
  import Header from './components/Header.vue'
  import Template from './components/Body.vue'
  import Footer from './components/Footer.vue'
  
  const estado = reactive({
    num1: '',
    num2: '',
    operacao: '--',
    erro: '',
  })

  const calcularResultado = computed(() => {
    estado.erro = ''
    const { num1, num2, operacao } = estado

    
    if (num1 === '' || num2 === '') {
      return '---'
    }

    
    if (operacao === '--') {
      estado.erro = 'É preciso selecionar um operador'
      return 'Erro'
    }

    const numero1 = Number(num1)
    const numero2 = Number(num2)

    switch (operacao) {
      case 'somar':
        return numero1 + numero2;
      case 'diminuir':
        return numero1 - numero2;
      case 'dividir':
        if (numero2 === 0) {
          estado.erro = 'Não é possível dividir por zero.'
          return 'Erro'
        }
        return (numero1 / numero2).toFixed(2);
      case 'multiplicar':
        return numero1 * numero2;
      default:
        estado.erro = 'Operação inválida.'
        return 'Erro'  
    }
  })
</script>
<template>
  <div class="calculator-container">
    <div class="calculator-card">
      <Header />
      <Template :calcular-resultado="calcularResultado" :estado="estado"/>
      <Footer />
    </div>
  </div>
</template>
