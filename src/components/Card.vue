<!-- usar : para buscar dentro do o bjeto character -->
<template>
  <div class="logo">
    <img
      src="/src/assets/images/Rick_and_Morty.svg.png"
      alt=""
      id="logoRickMorty"
    />
  </div>
  <div class="containerCards">
    <div v-for="character in characters" :key="character.id" class="col-md-4">
      <div class="card" style="width: 18rem">
        <img :src="character.image" alt="" />

        <div class="card-body">
          <h5 class="card-title">
            <b> {{ character.name }} </b>
          </h5>
          <p class="card-text">Status: {{ character.status }}</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">
            <b> Espécie </b><br />
            {{ character.species }}
          </li>
          <li class="list-group-item">
            <b> Gênero </b> {{ character.gender }}
          </li>
          <li class="list-group-item">
            <b> Localização atual </b> {{ character.location.name }}
          </li>
          <li class="list-group-item">
            <b> Aparições </b> <br />
            {{ character.episode.length }} episódios
          </li>
        </ul>
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
    axios.get("https://rickandmortyapi.com/api/character").then((response) => {
      console.log(response);
      this.characters = response.data.results;
    });
  },
};
</script>

<style scoped>
.containerCards {
  margin: auto;
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* 4 colun*/
  gap: 10px;
  width: 80vw;
  margin-bottom: 50px;
}

@media (max-width: 1024px) {
  .containerCards {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 768px) {
  .containerCards {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .containerCards {
    grid-template-columns: 1fr;
  }
}

.container {
  display: inline-flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

.list-group-item {
  font-family: "Hind", sans-serif;
  display: flex;
  flex-direction: column;
  border: none;
  padding: 5;
}

* {
  font-family: "Montserrat", sans-serif;
}

h1 {
  font-weight: 600;
  padding: 3rem 3rem 3rem 0;
  width: fit-content;
}

h1:hover {
  color: chartreuse;
}

.card-title:hover {
  color: chartreuse;
}

.card:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  border-color: chartreuse;
}

.card-body {
  border-bottom: none;
}

.logo {
  display: flex;
  justify-content: center;
  padding: 5rem;
}

#logoRickMorty {
  width: 20rem;
}

.card {
  margin-bottom: 40px;
}
</style>
