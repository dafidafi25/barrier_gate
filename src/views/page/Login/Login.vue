<script setup>
import { ref, onMounted } from "vue";

const count = ref(0);

const increment = () => {
  console.log("tes");
  console.log(count.value);
  count.value++;
};

onMounted(() => console.log(`the initial count is ${count.value}`));
</script>

<template>
  <Card>
    <template #header> Ini header </template>
    <template #title> ini tes button </template>
    <template #content>
      <Button @click="increment"> Increment</Button>
    </template>
    <template #footer>
      {{ count }}
    </template>
  </Card>
</template>
