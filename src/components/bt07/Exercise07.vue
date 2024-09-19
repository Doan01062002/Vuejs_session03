<template>
  <div>
    <h3>Form</h3>
    <form @submit.prevent="submitForm" action="">
      <input type="text" />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>
<script setup>
const submitForm = () => {
  console.log("Form submission prevented!");
};
</script>
<style></style>
