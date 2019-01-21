<template>
  <div id="app">
    <Header :title="title"/>
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{ hello }}</h1>
    <ul>
      <li v-for="(item,index) in list" :key="index">{{index+1}} - {{item}}</li>
      <li v-for="(person,index) in people" :key="index">{{index}} - {{person.name}}</li>
      <li v-for="(value,index) in profile" :key="index">{{index}} - {{value}}</li>
    </ul>
    <HelloWorld v-for="person in people" :key="person.id" msg="Welcome to Your Vue.js App xD xD"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";

export default {
  name: "app",
  data() {
    return {
      hello: "Hello World",
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
    HelloWorld,
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
