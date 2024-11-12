<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faTrashCan } from '@fortawesome/free-solid-svg-icons'

defineProps<{
  id: string
  note: string
}>()
</script>
<template>
  <div class="note" :title="id">
    <p>{{ note }}</p>
    <div class="delete-btn-wrapper">
      <button class="delete-btn">
        <FontAwesomeIcon :style="{ color: 'red' }" :icon="faTrashCan" />
      </button>
    </div>
  </div>
</template>
<style lang="scss">
.note {
  border: 1px solid black;
  border-radius: 10px;
  display: flex;
  flex: 0 1 auto;
  padding: 10px;
  justify-content: space-between;

  .delete-btn-wrapper {
    border-radius: 2px;
    margin-left: 4px;
    transition: 0.2s;
    &:hover {
      box-shadow: 0 0 1px 1px;
      background-color: rgb(238, 238, 238);
    }

    &:active {
      background-color: rgb(206, 206, 206);
    }
  }

  .delete-btn {
    background: none;
    border: none;

    transition: 0.1s;
    cursor: pointer;

    &:active {
      box-shadow: 0 -3px 1px 1px rgb(166, 166, 166);
      transform: translateY(1px) scale(0.95);
    }
  }
}
p {
  margin: 0;
}
</style>
