<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <h2>Make an input</h2>
  <p>{{ msg }}</p>
  <input type="text" />
  <button>Submit Note</button>
</template>

<style scoped lang="scss"></style>
