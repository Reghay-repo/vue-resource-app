<template>
  <div class="col-sm-12 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body note">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Note"
}
</script>

<style scoped>
  .panel-body {
    font-family: 'Architects Daughter', cursive;
    font-size: 24px;
    color: cadetblue;
  }

  .note {
    cursor: pointer;
  }
  .note:hover {
    background-color: chocolate;
    color: azure;
  }
</style>