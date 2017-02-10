<template>
  <div id="completed-todos">
    <h3>Completed Todos <small v-if="completed.length > 0">({{completed.length}})</small></h3>
    <ul class="list-group">
      <li class="list-group-item" v-if="completed.length == 0">Nothing has been done...</li>
      <li class="list-group-item" v-for="todo in completed">
        {{todo.body}}
        <button type="button" @click="remove(todo)" class="btn btn-default btn-sm">
        <span class="glyphicon glyphicon-remove-circle"></span> Remove
        </button>
      </li>
    </ul>
	</div>
</template>

<script>
export default{
  methods: {
    remove(todo){
      this.$store.dispatch('removeTodo', todo)
    }
  },
  computed: {
    completed(){
      return this.$store.getters.completedTodos
    }
  }
}
</script>
