<template>
  <div>
    <img :src="currentImage" alt="Random image" />
    <button @click="changeImage">Change image</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const images = [
  "https://vcdn1-dulich.vnecdn.net/2021/07/16/1-1626437591.jpg?w=460&h=0&q=100&dpr=2&fit=crop&s=i2M2IgCcw574LT-bXFY92g",
  "https://media-cdn-v2.laodong.vn/storage/newsportal/2023/8/26/1233821/Giai-Nhi-1--Nang-Tre.jpg",
  "https://d1hjkbq40fs2x4.cloudfront.net/2016-01-31/files/1045.jpg",
  "https://img.pikbest.com/origin/09/19/03/61zpIkbEsTGjk.jpg!w700wp",
];

const currentImage = ref(images[0]);

const changeImage = () => {
  const randomIndex = Math.floor(Math.random() * images.length);
  currentImage.value = images[randomIndex];
};
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>
