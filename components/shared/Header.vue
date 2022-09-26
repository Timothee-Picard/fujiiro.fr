<template>
  <header>
    <nuxt-link :to="{ name: 'index' }">Home</nuxt-link>
    <nuxt-link :to="{ name: 'about' }">Create</nuxt-link>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
header {
  position: absolute;
  width: 100%;
  background-color: rgba(255, 0, 0, 0.53);
  padding: 20px;
}
</style>
