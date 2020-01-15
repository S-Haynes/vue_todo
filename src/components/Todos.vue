<template>
  <div class="todos">
    <input type="text" v-model="newTodo">
    <button @click="onSubmit">Add Todo</button>
    <ul>
      <li v-for="(item, i) in todos" :key="item.text + i">{{ item.text }} <span @click="onDelete(item.id)">X</span> </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todos',
  props: ["todos"],
  data() {
    return {
      newTodo: ''
    }
  },
  methods: {
    onSubmit() {
      const newTodo = {
        text: this.newTodo, 
        id: this.todos.length + 1 
      }

      this.todos = [...this.todos, newTodo];
    },
    onDelete(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style scoped>
  li {
    text-align: left;
  }
</style>