<script>
/* eslint-disable */
import Container from 'src/components/Container.vue'
import NoteCard from 'src/components/NoteCard.vue'
import { useLocalNotes } from 'src/helper'
import { defineComponent } from 'vue'
import { useRouter } from 'vue-router'

export default defineComponent({
  components: { NoteCard, Container },
  name: 'PageIndex',
  setup() {
    const notes = useLocalNotes()
    const router = useRouter()
    return { router, notes }
  }
})
</script>

<template>
  <q-page padding>
    <Container>
      <div class="row items-center justify-between">
        <h3 class="text-blue-grey-9">Your notes</h3>
        <div>
          <q-btn round color="positive" icon="add" to="/new"></q-btn>
        </div>
      </div>

      <NoteCard
        v-for="({ title, description }, idx) in notes"
        :key="idx"
        :title="title"
        :description="description"
        @click="router.push(`/note/${idx}`)"
      />
      <div class="no-notes absolute-center" v-if="notes.length === 0">
        <q-icon name="check" size="100px" color="primary" />
        <div class="text-h5 text-primary text-center">
          You have not created any notes.
        </div>
      </div>
    </Container>
  </q-page>
</template>
<style scoped>
.no-notes {
  opacity: 0.5;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
