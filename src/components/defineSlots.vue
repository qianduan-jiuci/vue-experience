<script setup lang="ts">
import { useSlots } from "vue";

defineSlots<{
  default: (props: { id: number }) => void;
  name: (props: { message: string }) => any;
}>();
const slot = useSlots();
console.log(slot);
</script>

<template>
  <slot name="default" :id="1334"></slot>
  <slot name="name" :message="'se'" />
</template>

<style scoped></style>
