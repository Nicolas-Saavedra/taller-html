<template>
  <div class="container-fluid col-6 mb-5">
    <h2 class="title">Subscribe to my newsletter</h2>
    <form>
      <div class="mb-3 mt-5">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
        <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
      </div>
      <button type="submit" class="btn btn-primary" onclick="alert('You have suscribed successfully to my newsletter')">Subscribe</button>
    </form>
  </div>
</template>

<style scoped>

.title {
  font-size: 3rem;
}
.btn {
  display: grid;
  margin: auto;
}

</style>

<script setup lang="ts">

</script>