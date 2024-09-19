<template>
  <div>
    <input
      ref="inputRef"
      type="text"
      @keydown="handleKeydown"
      v-model="inputValue"
      placeholder="Nhập văn bản ở đây"
    />
  </div>
</template>

<script setup>
import { ref } from "vue";

const inputValue = ref("");
const inputRef = ref(null);

const handleKeydown = (event) => {
  if (event.key === "Enter") {
    if (event.shiftKey) {
      alert(inputValue.value);
      inputValue.value = "";
    } else {
      alert("Bạn cần nhấn Shift + Enter");
    }
    event.preventDefault();
  }
};
</script>

<style scoped></style>
