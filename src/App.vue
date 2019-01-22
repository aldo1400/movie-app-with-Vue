<template>
  <div id="app">
    <Header :title="title"/>
    <router-view/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "app",
  data() {
    return {
      title: "Vue movie DB APP1",
      list: ["Penguin", "Turtle", "Red Panda"],
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
