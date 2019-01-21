<template>
  <div id="app" v-if="status==='Ready'">
    <Header :title="title"/>
    <MoviesList/>
  </div>
  <div v-else-if="status==='Loading'">Loading</div>
  <div v-else>Error</div>
</template>

<script>
import Header from "./components/Header.vue";
import MoviesList from "./components/MoviesList.vue";

export default {
  name: "app",
  data() {
    return {
      hello: "Hello World",
      title: "Vue movie DB APP1",
      list: ["Penguin", "Turtle", "Red Panda"],
      isTrue: true,
      status: "Ready",
      people: [
        { id: 1, name: "Scott" },
        { id: "2", name: "Courtney" },
        { id: "3", name: "Aldo" }
      ],
      profile: {
        name: "Scott",
        age: 32,
        job: "Devepoler"
      }
    };
  },
  components: {
    MoviesList,
    Header
  }
};
</script>

<style >
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
}
</style>
