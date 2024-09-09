<script setup lang="ts">
defineProps<{
  note: string
}>()
</script>
<template>
  <div class="note">
    <p>{{ note }}</p>
  </div>
</template>
<style lang="scss">
.note {
  border: 1px solid black;
  border-radius: 10px;
  padding: 10px;
}
p {
  margin: 0;
}
</style>
