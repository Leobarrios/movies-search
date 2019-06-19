<template>
  <div id="app">
    <Navbar/>
    <Content/>
    <h1>{{titulo}}</h1>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld v-bind:msg="titulo" />
    
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue"
import Content from "./components/Content.vue"
import List from "./components/List.vue"

export default {
  name: "app",
  components: {
    HelloWorld,
    Navbar,
    Content,
    List,
  },
  data() {
    return {
      titulo: 'proyecto vue cli'
    }
  }

};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
