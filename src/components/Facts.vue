<template>
  <div>
    <ul>
      <li class="list" v-for="(item, index) in dados" :key="item.id">
        <div class="card">
          <img class="pics" :src="pics[index].url" :alt="pics[index].id">
          <div class="text">{{ item.text }}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'FactsText',

  data() {
      return {
        dados: [],
        pics: []
      }
    },

    methods: {
      async getData() {
        try {
            const response = await axios.get('https://cat-fact.herokuapp.com/facts');
            //console.log(response.data); // Verifica a resposta da API
            this.dados = response.data;
        } catch (error) {
            console.log(error);
        }
      },

      async getPic() {
        try {
            const response = await axios.get('https://api.thecatapi.com/v1/images/search?limit=10');
            const images = response.data.slice(0, 5);
            console.log(response.data); // Verifica a resposta da API
            this.pics = images;
        } catch (error) {
            console.log(error);
        }
      }
    },

    created() {
      this.getData();
      this.getPic();
    }
}
</script>

<style scoped>

ul {
  display: flex;
  flex-wrap: wrap;
}

.card {
  background-color: #222222;
  color: #F3EFE0;
  width: 20rem;
  margin: 10px;
  border-radius: 1rem;
  border: 1px solid black;
  margin-bottom: 1em;
  padding: 1em;
}

.text {
  margin: 0.5rem 0;
}

.list {
  gap: 1rem;
  list-style-type: none;
  font-size: 0.8rem;
}

.pics {
  max-width: 100%;
  max-height: 100%;
}

</style>
