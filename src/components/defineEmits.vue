<script setup lang="ts">
import { ref } from "vue";

const id = ref<number>(10);
// before
// const emit = defineEmits<{
//   (e: "count", id: number): void;
// }>();
// after
const emit = defineEmits<{
  count: [id: number];
}>();
const count = () => {
  id.value++;
  emit("count", id.value);
};
</script>

<template>
  {{ id }}
  <button @click="count">defineEmits</button>
</template>

<style scoped></style>
