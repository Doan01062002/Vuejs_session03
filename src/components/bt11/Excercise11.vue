<template>
  <div>
    <div :class="{ active: color }" :style="{ backgroundColor: red }"></div>
    <button @click="handleChangeBackground">Change background</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const color = ref(true);
const red = "red";
const handleChangeBackground = () => {
  color = false;
};
</script>
<style scoped>
.active {
  width: 100px;
  height: 100px;
  background-color: blue;
}
</style>
