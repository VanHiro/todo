<template>
  <div class="form pt-6">
    <todo-input @insert="newTodo" />
    <todo-list :list="todoList" />
  </div>
</template>

<style>
@import "./assets/base.css";
</style>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import TodoInput from "./components/TodoInput.vue";
import TodoList from "./components/TodoList.vue";

export default defineComponent({
  components: { TodoInput, TodoList },

  data() {
    return {
      todoList: ["foo", "bar", "zup"],
    };
  },

  methods: {
    newTodo(input: string) {
      this.todoList.push(input);
    },
  },
});
</script>
