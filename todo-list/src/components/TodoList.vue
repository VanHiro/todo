<template>
    <div v-for="todo in todoList" :key="todo">
      <p>{{ todo }}</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        value: {
            type: String,
            default: ""
        }
    },
    computed: {
      todoList: {
        get() {
          return this.value;
        },
        set(value: String) {
          this.$emit("input", value);
        }
      }
    }
})
</script>
