<template>
  <div class="todo-container">
    <div class="todo-wrap">
      <TodoHeader/>
      <TodoList/>
      <TodoFooter/>
    </div>
  </div>
</template>

<script>
    //引入组件
    import TodoHeader from "./components/TodoHeader.vue";
    import TodoList from "./components/TodoList.vue";
    import TodoFooter from "./components/TodoFooter.vue";

    export default {
        //映射标签
        components: {
            TodoHeader,
            TodoList,
            TodoFooter
        }
    }

</script>

<style>
  .todo-container {
    width: 600px;
    margin: 0 auto;
  }

  .todo-container .todo-wrap {
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
</style>
