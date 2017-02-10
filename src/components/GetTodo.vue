<template>
  <div id="get-todo" class="container">
    <div class="input-group">
      <input class="form-control"
        :value="newTodo"
        @change="getTodo"
        placeholder="I need to...">
      <div class="input-group-btn">
        <button class="btn btn-primary" @click="addTodo"><span class="glyphicon glyphicon-new-circle"></span> Add Todo</button>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    methods: {
      getTodo(e) {
        this.$store.dispatch('getTodo', e.target.value);
      },
      addTodo() {
        this.$store.dispatch('addTodo');
        this.$store.dispatch('clearTodo');
      }
    },
    computed: {
      newTodo() {
        return this.$store.getters.newTodo;
      }
    }
  }
</script>
