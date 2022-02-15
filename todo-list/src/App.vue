<template>
  <div class="form pt-6">
    <todo-form-vue />
  </div>
</template>

<style>
@import './assets/base.css';
</style>

<script setup lang="ts">
  import TodoInput from './components/TodoInput.vue';
  import TodoListVue from './components/TodoList.vue';
  import TodoFormVue from './components/TodoForm.vue'; 

  export default{
    data() {
      return {
        form: {
          list: [],
          todoText:''
        }
      }
    }
  }
</script>