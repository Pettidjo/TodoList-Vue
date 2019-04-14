<template>
  <div class="todo-item" v-bind:class="{'is-completed':todo.completed}">
    <input type="checkbox" v-on:change="markComplete" />
    <p>{{todo.title}}</p>
    <button @click="$emit('del-todo', todo.id)" class="del">x</button>
  </div>
</template>

<script>
export default {
  name:"TodoItem",
  props:["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed
    }
  }
}
</script>

<style scoped>
  .todo-item {
    background: #F4F4F4;
    padding: 10px;
    border-bottom: 1px #CCC dotted;
  }

  .is-completed {
    text-decoration: line-through;
  }

  .del {
    background: #ff0000;
    color: #FFF;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
  }

  input[type="checkbox"] {
    display: inline-block;
  }
</style>
