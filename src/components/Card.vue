<!-- usar : para buscar dentro do o bjeto character -->
<template>
  <div class="container">
  <h1>Listagem de Personagens</h1>
  <div class="containerCards">
    <div v-for="character in characters" :key="character.id" class="col-md-4">
      <div class="card" style="width: 18rem">
        <img :src="character.image" alt="" />

        <div class="card-body">
          <h5 class="card-title">Nome: {{ character.name }}</h5>
          <p class="card-text">Status: {{ character.status }}</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"> <b> Espécie </b><br> {{ character.species }}</li>
          <li class="list-group-item"> <b> Gênero </b> {{ character.gender }}</li>
          <li class="list-group-item">
           <b> Localização atual </b> {{ character.location.name }}
          </li>
          <li class="list-group-item">
            Aparições: {{ character.episode.length }} episódios
          </li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link">Card link</a>
          <a href="#" class="card-link">Another link</a>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      characters: [],
    };
  },
  mounted() {
    axios
      .get("https://rickandmortyapi.com/api/character")
      .then((response) => {
        console.log(response);
        this.characters = response.data.results;
      })
      .catch((error) => {
        console.error(error);
      });
  },
};
</script>

<style scoped>
.containerCards {
  display: grid;
  grid-template-columns: repeat(
    4,
    1fr
  ); /* Define quatro colunas de tamanho igual */
  gap: 10px;
  margin-left: 0;
  justify-content: space-between;
  background-color: aqua;
}

.container{
  display: inline-flex;
  flex-direction: column;

}

.list-group-item{
  font-family: 'Hind', sans-serif;
  display: flex;
  flex-direction: column;
}

* {
  font-family: 'Montserrat', sans-serif;
}

h1{
  font-weight: 500;
}

</style>
