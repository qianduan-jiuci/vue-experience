<script setup lang="ts">
import { toRef, watchEffect } from "vue";

const props = defineProps<{
  // msg: string;
  foo: {
    bar: string;
  };
}>();

useXXX(toRef(props.foo, "bar"));
function useXXX(value: any) {
  console.log(value);
  watchEffect(() => {
    console.log("watch effect: ", value);
  });
}
</script>

<template>{{ props }}</template>

<style scoped></style>
