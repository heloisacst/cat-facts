<template>
  <div class="about">
    <div class="text">
      <h1>Sobre este projeto</h1>
      <p>Esta página foi feita para estudar o framework Vue.JS e em paralelo, buscar dados de duas APIs.</p>
      <p>Link das APIs:</p>
        <div> 
          <ol><a href="https://cat-fact.herokuapp.com">https://cat-fact.herokuapp.com</a></ol>
          <ol><a href="https://api.thecatapi.com">https://api.thecatapi.com</a></ol>
        </div>
    </div>
  </div>
</template>

<style scoped>

.about {
  display: flex;
  justify-content: center;
  align-items: center;
  color: wheat;
  height: 100%;
}

.text {
  text-align: center;
}

 ol {
  margin: 0;
 }

 a {
  text-decoration: none;
  color: wheat;
 }

</style>
