<template>
  <div class="form-group">
    <label class="mr-2 font-bold text-grey">TODO item</label>
    <input
      type="text"
      class="input"
      v-model="todoText"
      placeholder="Lear Go language"
    />
  </div>
</template>

<script  setup lang="ts">
import { defineComponent } from 'vue'

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
    data() {
        return {
            
        }
    }
})
</script>
