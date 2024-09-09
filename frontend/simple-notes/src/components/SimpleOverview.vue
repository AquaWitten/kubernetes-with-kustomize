<script setup lang="ts">
import SimpleNote from './SimpleNote.vue'

defineProps<{
  notes: string[]
}>()
</script>
<template>
  <div v-for="note in notes" :key="note">
    <SimpleNote :note="note" />
  </div>
</template>
