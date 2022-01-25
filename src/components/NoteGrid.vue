<template>
  <div class="row">
      <note v-for="(note,index) in notes" @click.native="deleteNote(index)">
        {{ note }}
      </note>
  </div>
</template>

<script>
import Note from "./Note.vue";

export default {
  name: "NoteGrid",
  props: ['notes'],
  components: {
    Note
  },
  methods:{
    deleteNote(index){
      this.$emit('noteDeleted', index)
    }
  }
}
</script>

<style scoped>

</style>