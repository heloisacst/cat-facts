<template>
  <nav>
    <router-link to="/" class="nav-link">Home</router-link>
    <router-link to="/about" class="nav-link">Sobre</router-link>
  </nav>
</template>

<script>
  export default {
    name: 'NavBar'
  }
</script>

<style scoped>
  .nav-link {
    color: wheat;
  }
</style>