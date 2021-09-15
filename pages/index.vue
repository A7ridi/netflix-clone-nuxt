<template>
  <div class="home">
    <Hero />
  </div>
</template>

<script>
export default {
  data() {
    return {
      movies: [],
    }
  },
  methods: {
    async getMovies() {
      const data = axios.get(
        'https://api.themoviedb.org/3/movie/now_playing?api_key=d0d3b9b8ff1204a42d67cff655e90361&language=en-US&page=1'
      )
      const result = await data
    },
  },
}
</script>
