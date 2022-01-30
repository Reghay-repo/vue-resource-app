<template>
    <div class="container">
       <div class="row">
       <div class="col-md-6 col-lg-offset-3 ">
           <div class="title">contact info</div>

         <div class="form-group">
           <div class="form-label">Name</div>
           <input type="text" v-model="user.name" class="form-control">
         </div>

         <div class="form-group">
           <div class="form-label">Email</div>
           <input type="email" v-model="user.email" class="form-control">
         </div>

         <div class="form-group">
           <div class="form-label">Phone number</div>
           <input type="number" v-model="user.phone" class="form-control">
         </div>

         <div class="form-group">
           <button class="btn btn-primary" @click="dataLog">submit</button>
         </div>
       </div>
       </div>
    </div>
</template>

<script>
    export default {
      data() {
        return {
          user : {
            name: '',
            email: '',
            phone: ''
          }
          }
      },
      methods:{
          dataLog() {
            console.log(this.user)
          }
        }
    }
</script>

<style scoped>

</style>
