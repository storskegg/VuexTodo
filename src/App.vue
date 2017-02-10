<template>
  <div id="app" class="container">
    <div class="row">
      <GetTodo class="col-xs-12"></GetTodo>
    </div>
    <div class="row">
      <CurrentTodos class="col-sm-8"></CurrentTodos>
      <CompletedTodos class="col-sm-4"></CompletedTodos>
    </div>
  </div>
</template>

<script>
import GetTodo from './components/GetTodo.vue';
import CurrentTodos from './components/CurrentTodos.vue';
import CompletedTodos from './components/CompletedTodos.vue';
//bump
export default {
  components: {
    GetTodo,
    CurrentTodos,
    CompletedTodos
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

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
