<template>
  <div>
    <a href="https://www.google.com" @click.prevent="checkLink($event)">
      Liên kết đến Google (https)
    </a>
    <br />
    <a href="http://www.google.com" @click.prevent="checkLink($event)">
      Liên kết đến Google (http)
    </a>
  </div>
</template>

<script setup>
const checkLink = (event) => {
  const url = event.target.getAttribute("href");
  if (!url.startsWith("https://")) {
    alert("Đường dẫn không hợp lệ");
  } else {
    window.location.href = url;
  }
};
</script>

<style>
.error {
  color: red;
  font-weight: bold;
}
</style>
