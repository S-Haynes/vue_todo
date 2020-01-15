<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Todos :todos="todos"/>
  </div>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        { text: "buy food",
          id: 1 
        },
        { 
          text: "buy drinks",
          id: 2
        },
        { 
          text: "buy sandals",
          id: 3 
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
