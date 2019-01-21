<template>
  <div>{{movie.title}}</div>
</template>

<script>
export default {
  name: "MoviesList",
  data() {
    return {
      movie: {}
    };
  },
  created: function() {
    this.fetchData();
  },
  methods: {
    fetchData: async function() {
      try {
        const res = await fetch(
          "https://api.themoviedb.org/3/movie/550?api_key=63222e52f9045dc57b20e736f605be66"
        );
        const movie = await res.json();
        this.movie = movie;
      } catch (e) {
        console.log(e);
      }
    }
  }
};
</script>

<style>
</style>
