<template>
  <div class="home">
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:del-todo= "deleteTodo"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import Todos from '../components/Todos.vue';
import AddTodo from '../components/AddTodo.vue';

export default {
  name: 'home',
  components: {
    // HelloWorld,
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Todo one',
          completed: false,
        },
        {
          id: 2,
          title: 'Todo two',
          completed: true,
        },
        {
          id: 3,
          title: 'Todo three',
          completed: false,
        },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id);
    },
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];
    }
  }
};
</script>
<style scoped>

</style>

