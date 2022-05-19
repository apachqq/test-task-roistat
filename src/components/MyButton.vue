<template>
    <button class="btn" @click="this.isOpen = !this.isOpen"><slot></slot></button>
</template>

<script>
    export default {
        name: 'my-button'
    }
</script>

<style scoped>
    .btn {
        border-radius: 8px;
        border: 1px solid black;
        padding: 5px 15px;
        margin: 10px;
        font-size: 10px;
    }
</style>
