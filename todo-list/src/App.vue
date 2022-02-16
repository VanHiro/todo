<template>
  <div class="form pt-6">
    <todo-form-vue />
  </div>
</template>

<style>
@import './assets/base.css';
</style>

<script lang="ts">
  import TodoFormVue from './components/TodoForm.vue'; 

  export default {
    name: "Todo",
    components: {
      TodoFormVue
    }
  };
</script>