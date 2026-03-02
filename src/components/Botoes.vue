<script setup>
const emit = defineEmits(['clicou'])
</script>

<template>

<div class="botoes">

    <button @click="emit('clicou', '7')">7</button>
    <button @click="emit('clicou', '8')">8</button>
    <button @click="emit('clicou', '9')">9</button>
    <button @click="emit('clicou', '+')">+</button>

    <button @click="emit('clicou', '4')">4</button>
    <button @click="emit('clicou', '5')">5</button>
    <button @click="emit('clicou', '6')">6</button>
    <button @click="emit('clicou', '-')">-</button>

    <button @click="emit('clicou', '1')">1</button>
    <button @click="emit('clicou', '2')">2</button>
    <button @click="emit('clicou', '3')">3</button>
    <button @click="emit('clicou', '*')">*</button>

    <button @click="emit('clicou', '0')">0</button>
    <button @click="emit('clicou', 'C')">C</button>
    <button @click="emit('clicou', '=')">=</button>
    <button @click="emit('clicou', '/')">/</button>
    

</div>

</template>

<style scoped>
.botoes{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 14px;

    button {
    height: 60px;
    background: #1f1f1f;
    color: rgb(169, 169, 169);

    box-shadow: 
    6px 6px 10px #141414,
    -6px -6px 10px #2a2a2a;
}

    button:active {
    box-shadow: 
    inset 6px 6px 10px #141414,
    inset -6px -6px 10px #2a2a2a;
}
}
</style>