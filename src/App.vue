<template>
  <div id="app">
   
  <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
export default {
  name: 'App',
  components: {
    TodoList
  },
  // data function avails data to the template
  data() {
    return {
      todos: [{
        title: 'Todo A',
        project: 'Project Nice',
        done: false,
      }, {
        title: 'Todo B',
        project: 'Project Bad',
        done: true,
      }, {
        title: 'Todo Cool',
        project: 'Project C',
        done: false,
      }, {
        title: 'Todo D',
        project: 'Project Demanding',
        done: false,
      }],
    };
  },
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
