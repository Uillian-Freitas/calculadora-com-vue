<script setup>

defineProps(['valor'])

</script>

<template>
    <div class="display">
        {{ valor }}
    </div>
</template>

<style scoped>

.display{
    height: 80px;
    border-radius: 14px;
    margin-bottom: 20px;
    padding: 16px;

    background: #1f1f1f;
    color: #00ff9d;
    font-size: 2.4rem;
    text-align: right;
    font-family: 'Courier New', monospace;

    display: flex;
    align-items: center;
    justify-content: flex-end;

    box-shadow:
    inset 6px 6px 10px #141414,
    inset -6px -6px 10px #2a2a2a;
}

</style>