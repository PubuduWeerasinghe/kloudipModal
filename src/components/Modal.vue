<template>
    <div v-if="isOpen" class="top-container">
        <div class="main-container">
        <h1>Modal Title</h1>
        <p>Test content</p>
        <button @click="emits('onClose')">Cancel</button>
        <button>Confirm</button>
    </div>
    </div>
    
</template>
<script lang="ts" setup>

const emits = defineEmits<{onClose: []}>()
defineProps<{ isOpen; boolean }>()

</script>
<style scoped>
.main-container{
    padding: 20px;
    background: #fff;
    border: 2px solid #fff;
    border-radius: 5px;
    width: 400px;
    height: 200px;
    color: black;
}
.top-container{
    height: 100%;
    width: 100%;
    z-index: 9999;
    position: fixed;
}
</style>