<template>
  <div class="row">
    <form>
    <div class="col-sm-8 col-xs-12 col-md-6 col-sm-offset-2 col-md-offset-3 form-group">
      <label for="note">Note</label>
      <textarea  v-model="note" id="note" cols="30" rows="3" class="form-control"></textarea>
    </div><div class="col-sm-8 col-xs-12 col-md-6 col-sm-offset-2 col-md-offset-3 form-group">
      <button class="btn btn-info" @click.prevent="addNote">create note</button>
    </div>
    </form>
  </div>

</template>

<script>
export default {
  name: "AddNote",
  data() {
    return {
      note:''
    }
  },
  methods:{
    addNote(){
      this.$emit('noteAdded', this.note);
      this.note = ''
    }
  }

}
</script>

<style scoped>

</style>