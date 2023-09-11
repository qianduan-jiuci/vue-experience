<script setup lang="ts">
const props = defineProps<{
  modelValue: string;
}>();
const emits = defineEmits<{
  "update:modelValue": [value: string];
}>();
const onInput = (e: any) => {
  emits("update:modelValue", e.target.value);
};
</script>

<template>
  <input type="text" :value="props.modelValue" @input="onInput" />
</template>

<style scoped></style>
