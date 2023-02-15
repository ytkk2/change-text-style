<template>
<div :class="{ textVertical: isActive }">
  <textarea class="textArea"></textarea>
</div> 
  <button @click="swichToVertical">change</button>
 
</template>

<script setup>
import { ref } from 'vue'

const isActive = ref(false)
const swichToVertical = () => {
 isActive.value = !isActive.value
}
</script>

<style>
.textVertical {
  writing-mode:  vertical-rl;
}
</style>
