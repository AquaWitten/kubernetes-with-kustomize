<script setup lang="ts">
import { ref } from 'vue'
import SimpleInput from './components/SimpleInput.vue'
import SimpleOverview from './components/SimpleOverview.vue'
import { v4 } from 'uuid'
import type { Note } from './interfaces/Note'

const noteArr = ref<Note[]>([])
const text = ref('')

const getStoredNotes = () => {}

const handleSubmit = () => {
  const uuid = v4()
  const note: Note = { id: uuid, note: text.value }
  noteArr.value.push(note)
  text.value = ''
}
</script>

<template>
  <div class="main-content">
    <header>
      <h1>Simple Notes</h1>
      <p>Enter your notes here to store them</p>
    </header>
    <main>
      <SimpleInput v-model="text" @save-note="handleSubmit" />
      <hr />
      <SimpleOverview :notes="noteArr" />
    </main>
  </div>
</template>

<style scoped lang="scss">
.main-content {
  font-family: 'Roboto', sans-serif;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: center;
  margin: auto;
  width: 60%;
  height: 100%;
}
header,
main {
  border: 3px solid #cb3ccb;
  border-radius: 25px;
  width: 100%;
  align-items: center;
  display: flex;
  flex-flow: column;
}
header {
  margin-top: 80px;
  h1 {
    color: orange;
    margin: 16px 0 0 0;
  }
}
main {
  margin: 48px 0;
  flex: 1 0 auto;

  hr {
    display: block;
    height: 1px;
    border: 0;
    border-top: 3px solid #cb3ccb;
    margin: 1em 0;
    padding: 0;
    width: 90%;
  }
}
</style>
