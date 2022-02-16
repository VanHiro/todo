<template>
  <div class="form-group">
    <label class="mr-2 font-bold text-grey">TODO item</label>
    <input
      type="text"
      class="input"
      v-model="todoText"
      placeholder="Lear Go language"
      @input="v.$touch()"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        value: {
            type: String,
            default: ""
        },
        v: {
            type: Object,
            required: true
        }
        
    },
    computed: {
      todoText: {
        get() {
          return this.value;
        },
        set(value: String) {
          this.v.$touch();
          this.$emit("input", value);
        }
      }
    }
})
</script>
