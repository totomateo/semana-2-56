<template>
  <div>
    <div class="card" v-for="(movie, index) of movies" :key="index">
      <img src="movie.Poster" class="card-img-top" alt="movie Poster" />
      <div class="card-body">
        <h2 class="card-title">{{ movie.Title }}</h2>
        <hr />
        <p class="card-text">Tipo de produccion: {{ movie.Type }}</p>
        <p>Año: {{ movie.Year }}</p>
        <a :href="'https://www.imdb.com/title/'+ 'movie.imdbID'  " class="btn btn-primary"
          >Mas info</a
        >
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get(
        "http://www.omdbapi.com/?s=The+lord+of+the+Rings&type=movie&apikey=d3688b9a "
      )
      .then((response) => (this.movies = response.data.Search.slice(0, 4)));
  },
};
</script>
<style scoped>
</style>