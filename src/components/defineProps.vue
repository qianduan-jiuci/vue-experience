<script setup lang="ts">
import type { User } from "./defineProps";
const { username } = defineProps<User>();
</script>

<template>
  {{ username }}
</template>

<style scoped></style>
