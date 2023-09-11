<script setup lang="ts">
// defineProps

// import { ref } from "vue";
// import definePropsVue from "./components/defineProps.vue";
// const username = ref<string>("张");
// const password = ref<string>("1234");
// const update = () => {
//   username.value = "李四";
// };

// defineEmits
// import { ref } from "vue";
// import defineEmitsVue from "./components/defineEmits.vue";
// const countId = ref<number>(0);
// const count = (id: number) => {
//   countId.value = id;
// };

// defineSlots
// import defineSlotsVue from "./components/defineSlots.vue";

// defineModel

// import { ref, watch } from "vue";
// import defineModelVue from "./components/defineModel2.vue";
// const input = ref<string>("input");
// // const onInput = (value: string) => {
// //   input.value = value;
// // };
// watch(input, () => {
//   console.log("input");
// });

// toRef and toValue
import { ref } from "vue";
import ToRefAndToValue from "./components/ToRefAndToValue.vue";
const foo = ref<{
  bar: string;
}>({
  bar: "barbar",
});

// window.msg = msg;
</script>

<template>
  <!-- <definePropsVue :username="username" :password="password" />
  <button @click="update">修改username</button> -->

  <!-- {{ countId }}
  <defineEmitsVue @count="count"></defineEmitsVue> -->

  <!-- <defineSlotsVue>
    <template #default="{ id }">
      {{ id }}
    </template>
    <template #name="{ message }">
      {{ message }}
    </template>
  </defineSlotsVue> -->

  <!-- <defineModelVue :input-value="input" @updateModelValue="onInput"></defineModelVue> -->
  <!-- <defineModelVue v-model="input"></defineModelVue> -->

  <ToRefAndToValue :foo="foo"></ToRefAndToValue>
</template>

<style scoped></style>
