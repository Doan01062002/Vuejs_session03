<template>
  <div>
    <p :id="elementId" :class="elementClass">
      Đây là một đoạn văn với id và class được gán từ biến.
    </p>
  </div>
</template>

<script setup>
const elementId = "unique-element-id";
const elementClass = "text-primary font-bold";
</script>

<style>
.text-primary {
  color: blue;
}

.font-bold {
  font-weight: bold;
}
</style>
