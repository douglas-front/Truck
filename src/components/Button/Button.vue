<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    BgColor: {
      type: String,
      required: true
    },
    Color: {
      type: String,
      required: true
    },
    Text: {
      type: String,
      required: true
    }
  }
})
</script>
<template>
  <button :style="{ background: BgColor, color: Color }">{{ Text }}</button>
</template>

<style scoped>
button {
  cursor: pointer;
  padding: 1.2vw 4vw;
  border: none;
  font-size: 1vw;
}
</style>
