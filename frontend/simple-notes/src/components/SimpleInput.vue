<script setup lang="ts">
import { defineEmits } from 'vue'
const emit = defineEmits(['saveNote'])
const note = defineModel()

const handleSubmit = () => {
  emit('saveNote')
}
</script>

<template>
  <div class="simple-input">
    <h2>Make an input</h2>
    <label for="input-field">Enter a note </label>
    <input v-model="note" id="input-field" type="text" />
    <button @click="handleSubmit">Submit Note</button>
  </div>
</template>

<style scoped lang="scss">
.simple-input {
  margin: 16px 0;

  h2 {
    margin-top: 0;
  }
}
</style>
