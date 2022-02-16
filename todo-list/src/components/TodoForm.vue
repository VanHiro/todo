<template>
  <div class="form pt-6">
    <form>
      <todo-input-vue v-model="this.form.todoText" :v="this.form.todoText" />
      <button type="submit">Submit</button>
      <todo-list-vue />
    </form>
  </div>
</template>

<script lang="ts">
  import TodoInputVue from './TodoInput.vue';
  import TodoListVue from './TodoList.vue';

  export default {
    name: "FormComponent",
    components: {TodoInputVue, TodoListVue },

    data() {
        return {
            form: {
                todoText: String,
                todoList: Array
            }
        }
    },

    methods: {
      submit() {
        alert("Form submitted");
        this.form.todoList.push(this.form.todoText);
      },
    },
  }

    /*  
  const storage_key: string = "todo-list-items";

   const filters: object = {
      showAll: (todos) => todos
  }  
  */
  
</script>