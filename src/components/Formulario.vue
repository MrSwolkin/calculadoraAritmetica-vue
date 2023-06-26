<script setup>
    const props = defineProps(['primeiroNumber', 'segundoNumber', 'selecioneCalculo'])
    
</script>
<template>
    <form class="d-flex justify-content-center  border border-dark">
        <div class="row">
            <div class="col-md-3 p-5 m-5">
                <input @keyup="props.primeiroNumber" class="form-control p-2 fs-5" type="number"
                    placeholder="insira um número" required>
            </div>
            <div class="col-md-3 p-5 m-5">
                <input @keyup="props.segundoNumber" class="form-control p-2 fs-5" type="number"
                    placeholder="insira outro número" required>
            </div>
            <div class="col-md-3 p-5  m-5">
                <select @change="props.selecioneCalculo" class="form-select p-2 fs-5">
                    <option value="adicao">Adição</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>