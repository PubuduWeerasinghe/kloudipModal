<script setup>
import Modal from './components/Modal.vue';
import {ref} from 'vue'

const isOpen = ref(false);

//Open Popup
const openPopup =()=>{
  isOpen.value = true;
}

//Close Popup
const onClose =()=>{
  isOpen.value = false;
}
</script>

<template>
 <Modal :isOpen="isOpen" @onClose="onClose"/>
  <button @click="openPopup"><span style="color: white;">Open Popup Modal</span></button>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
