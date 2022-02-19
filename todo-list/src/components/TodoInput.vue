<template>
  <form class="form-group" @submit.prevent="submit">
    <label class="mr-2 font-bold text-grey">TODO item</label>
    <input type="text" class="input" v-model="input" placeholder="" />
    <button type="submit">Submit</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      input: "",
    };
  },

  methods: {
    submit() {
      this.$emit("insert", this.input);
      this.input = "";
    },
  },
});
</script>
