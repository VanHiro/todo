<script setup lang="ts">
import TodoInput from './components/TodoInput.vue';
</script>

<template>
  <header>
    <h1>Here you can find you todo list</h1>
  </header>
  <main>
    <div class="main input">
      <TodoInput />
    </div>
  </main>
</template>

<style>
@import './assets/base.css';
</style>
