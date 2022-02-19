<template>
  <div>
    <button @click="deleteAll()">Reset</button>
    <ul>
      <li v-for="(item, index) in list" :key="item">
        {{ item }}
        <button @click="deleteItem(index)">X</button>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import type { PropType } from "vue";

export default defineComponent({
  props: {
    list: Array as PropType<Array<string>>,
  },

  methods: {
    deleteItem(index: number) {
      this.list?.splice(index, 1);
    },

    deleteAll() {},
  },
});
</script>
