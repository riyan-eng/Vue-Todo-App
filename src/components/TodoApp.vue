<template lang="">
    <div class="container" style="max-width:600px">
        <h2 class="text-center mt-5">My vue todo app</h2>
        <div>
            <form @submit.prevent="addTodo">
                <label for="newTodo">New Todo</label>
                <input v-model="newTodo" type="text" name="newTodo" id="newTodo">
                <button type="submit" name="button">Add</button>
            </form>
        </div>
        <button @click="allDone" type="button" name="button">All Done</button>
        <div class="mt-3">
            <ul>
                <li v-for="todo in todos">
                  <input type="checkbox" v-model="todo.done">
                  <span :class="{ done: todo.done }">{{todo.title}}</span>
                  <button @click="removeTodo(todo)" type="button" name="button">Remove</button>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>

export default {
    name: 'TodoApp',
    data(){
        return {
            title: 'Hello Coding Garden',
            newTodo: '',
            todos: []
        }
    },
    methods: {
        addTodo() {
          this.todos.push({
            title: this.newTodo,
            done: false
          });
          this.newTodo = '';
        },
        removeTodo(todo) {
          const todoIndex = this.todos.indexOf(todo);
          this.todos.splice(todoIndex, 1);
        },
        allDone() {
          this.todos.forEach(todo => {
            todo.done = true;
          });
        }
      }
}
</script>
<style lang="">
    
</style>