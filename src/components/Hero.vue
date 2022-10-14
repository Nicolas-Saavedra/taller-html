<template>
  <div class="hero">
    <h1 class="title">Nicolas Saavedra</h1>
    <h3 class="subtitle">Student of "Universidad de los Andes"</h3>
  </div>
</template>

<style scoped>

.hero {
  height: 50vh;
  background: url('hero.jpg') no-repeat center center;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  font-size: 3rem;
  color: white;
  text-shadow: 8px 8px 8px rgba(0, 0, 0, 0.5);
}

.title {
  font-size: 5rem;
}

.subtitle {
  font-size: 2rem;
}

</style>

<script setup lang="ts">

</script>
