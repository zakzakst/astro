<script setup lang="ts">
import { ref } from "vue";

const { defaultCount = 0 } = defineProps<{ defaultCount?: number }>();
const count = ref(defaultCount);
const increment = () => (count.value += 1);
</script>

<template>
  <button @click="increment">
    <span>Count: {{ count }}</span>
  </button>
</template>
