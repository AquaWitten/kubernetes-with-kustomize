<script setup lang="ts">
import SimpleNote from './SimpleNote.vue'
import type { Note } from '../interfaces/Note'

defineProps<{
  notes: Note[]
}>()
</script>
<template>
  <div class="note-overview">
    <SimpleNote v-for="item in notes" :key="item.id" :note="item.note" :id="item.id" />
  </div>
</template>
<style lang="scss">
.note-overview {
  width: 90%;
  gap: 10px;
  height: 510px;
  margin-bottom: 16px;
  display: flex;
  flex-flow: column wrap;
  align-content: flex-start;
}
</style>
