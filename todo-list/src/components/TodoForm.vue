<template>
  <div class="form pt-6">
      <todo-input-vue v-model="form.todoText" :v="$v.form.todoText" />
      <div>
          <todo-list-vue v-model="form.list" :v="$v.form.list" />
      </div>
  </div>
</template>

<style>
@import './assets/base.css';
</style>

<script setup lang="ts">
  import TodoInputVue from './TodoInput.vue';
  import TodoListVue from './TodoList.vue';
  
  const storage_key: string = "todo-list-items";

  const filters: object = {
      showAll: (todos) => todos
  } 
  export default{
    name: "FormComponent",
    components: {TodoInputVue, TodoListVue},

    data() {
        return() {
            form: {
                todoText: "",
                list: []
            }
        }
    }
  }
</script>