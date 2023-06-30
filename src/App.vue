<script setup>
import Cabecalho from './components/Cabecalho.vue';
import Formulario from './components/Formulario.vue';
import Resultado from './components/Resultado.vue';
import { reactive } from 'vue';


const estado = reactive({
    number1: Number(''),
    number2: Number(''),
    calculo: 'adicao',
    resultado: '',
})


const adicao = () => {
    const resultadoAdicao = estado.number1 + estado.number2
    estado.resultado = resultadoAdicao;
    return estado.resultado
}

const subtracao = () => {
    const resultadoSubtracao = estado.number1 - estado.number2
    estado.resultado = resultadoSubtracao;
    return estado.resultado
}

const multiplicacao = () => {
    const resultadoMultiplicacao = estado.number1 * estado.number2
    estado.resultado = resultadoMultiplicacao;
    return estado.resultado
}

const divisao = () => {
    const resultadoDivisao = estado.number1 / estado.number2
    estado.resultado = resultadoDivisao;
    return estado.resultado
}

</script>

<template>
    <div class="container">
        <Cabecalho/>
        <Formulario :primeiroNumber="evento => estado.number1 = evento.target.value" :segundoNumber="evento => estado.number2 = evento.target.value" :selecioneCalculo="evento => estado.calculo = evento.target.value"/>
        <Resultado :selecioneCalculo="estado.calculo" :funcaoAdicao="adicao()" :funcaoSubtracao="subtracao()" :funcaoMultiplicacao="multiplicacao()" :funcaoDivisao="divisao()"/>
    </div>
</template>
