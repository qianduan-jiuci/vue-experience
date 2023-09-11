<script setup lang="ts">
const model = defineModel();
// defineModel的本质就是设置一个modelValue的props， 并当input事件触发的时候，发送update:modelValue的事件，将最新的值传送给父组件
</script>

<template>
  <input type="text" v-model="model" />
</template>

<style scoped></style>
