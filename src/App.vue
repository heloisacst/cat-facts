<template>
  <div id="app">
    <NavBar class="nav"/>
    <router-view/>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';

export default {
    components: { 
      NavBar 
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #434242;
  box-sizing: content-box;
}

 .nav {
  justify-content: center;
  
}

</style>
