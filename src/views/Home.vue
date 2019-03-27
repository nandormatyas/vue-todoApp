<template>
  <div class="home">
    <Todos v-bind:todos="todos" />
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue';
import Todos from '../components/Todos';

export default {
  name: 'home',
  components: {
    //HelloWorld,
    Todos,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo one",
          completed: false
        },
        {
          id: 2,
          title: "Todo two",
          completed: true
        },
        {
          id: 3,
          title: "Todo three",
          completed: false
        }


      ],
    }
  }
};
</script>
