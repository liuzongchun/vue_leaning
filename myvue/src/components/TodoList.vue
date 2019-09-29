<template>
  <div>
    <ul class="todo-main">
      <TodoItem v-for="(todo,index) in todos" :key="index" :todo="todo" :index="index" :deleteTodo="deleteTodo"/>
    </ul>
  </div>
</template>

<script>
    //引入组件
    import TodoItem from "./TodoItem.vue";

    export default {
        props: {
            todos: Array,
            deleteTodo: Function
        },
        components: {//声明标签
            TodoItem
        }
    }
</script>
<style>
  .todo-main {
    margin-left: 0px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
  }

  .todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
  }


</style>
