<script setup>
const props = defineProps(['selecioneCalculo', 'funcaoAdicao', 'funcaoSubtracao', 'funcaoMultiplicacao', 'funcaoDivisao'])
</script>

<template>
    <div
        class="row d-flex justify-content-center p-5 m-4 bg-secondary text-center text-body shadow p-3 mb-5 rounded border border-dark">
        <div class="col-md-3">
            <p class="text-white">Resultado =</p>
        </div>
        <div class="col-md-3">
            <p class="fw-bold text-white" v-if="props.selecioneCalculo === 'adicao'"> {{ props.funcaoAdicao }}</p>
            <p class="fw-bold text-white" v-else-if="props.selecioneCalculo === 'subtracao'">{{ props.funcaoSubtracao }}</p>
            <p class="fw-bold text-white" v-else-if="props.selecioneCalculo === 'multiplicacao'">{{ props.funcaoMultiplicacao }}</p>
            <p class="fw-bold text-white" v-else="props.selecioneCalculo === 'divisao'">{{ props.funcaoDivisao }}</p>
        </div>
    </div>
</template>

<style scoped>
p {
    font-size: 50px;
}   
</style>