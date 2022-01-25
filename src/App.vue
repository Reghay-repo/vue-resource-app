<template>
    <div class="container">
        <add-note @noteAdded="addNote"></add-note>
        <note-grid :notes="notes" @noteDeleted="deleteNote"></note-grid>
        <div class="row">
          <div class="col-xs-12 text-center">
              <div class="alert alert-info">
                Info: click on a Note to delete it !
              </div>
          </div>
        </div>
    </div>
</template>

<script>
    import NoteGrid from "./components/NoteGrid.vue";
    import AddNote from './components/AddNote.vue'
    export default {
      data() {
        return {
          notes: ['vue js is annoying'],
          maxNotes: 10
        }
      },
      components: {
        NoteGrid,
        AddNote
      },
      methods:{
        addNote(note) {
          this.notes.push(note);
        },
        deleteNote(index) {
          this.notes.splice(index)
        }
      }
    }
</script>

<style scoped>

</style>
