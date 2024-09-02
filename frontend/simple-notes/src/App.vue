<script setup lang="ts">
import SimpleInput from './components/SimpleInput.vue'
</script>

<template>
  <header>
    <h1>Simple Notes</h1>
    <p>Enter your notes here to store them</p>
    <SimpleInput msg="Input you text here to save it" />
  </header>

  <main></main>
</template>

<style scoped lang="scss">
header {
  h1 {
    color: orange;
  }
}
</style>
