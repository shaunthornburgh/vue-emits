<template>
  <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
    <h1 class="text-base font-semibold leading-7 text-gray-900 pt-8">Parent Component</h1>
    <p>Button has been clicked: {{ count }} times</p>
    <ChildComponent @clicked="increaseCount" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './components/ChildComponent.vue'

const count = ref(0)

function increaseCount() {
  count.value++
}
</script>