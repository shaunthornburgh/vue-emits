<template>
  <button
      @click="notifyParent"
      type="button"
      class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 mt-6"
  >Click me!</button>
</template>

<script setup>
import { defineEmits } from 'vue'

const emit = defineEmits(['clicked'])

function notifyParent() {
  emit('clicked')
}
</script>