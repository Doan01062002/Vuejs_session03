<template>
  <div>
    <div>
      <h3>Binding property</h3>
      <ul>
        <li>1. v-bind</li>
        <li>2. v-if, v-else, v-else-if</li>
        <li>3. v-for</li>
        <li>4. v-show</li>
        <li>5. v-model</li>
      </ul>
      <img v-bind:src="image" alt="" />
      <p>*********** v-if ***********</p>
      <!-- nếu điều kiện đúng thì render ra không thì sẽ không hiển thị trong dom -->
      <p v-if="isVif">Hiển thị khi điều kiện đúng</p>
      <p>************ v-show ***********</p>
      <!-- Nếu điều kiện đúng thì hiển thị trên màn màn hình còn sai thì display: none tức vẫn hiển thị trong dom -->
      <p v-show="isVshow">Hiển thị nếu điều kiện v-show thỏa mãn</p>
      <p>************ v-for ***********</p>
      <p>Hiển thị dữ liệu mảng</p>
      <ul>
        <li v-for="(student, index) in students" :key="index">
          {{ student.name }}
        </li>
      </ul>
      <p>************** v-model ************</p>
      <input type="text" v-model="inputText" />
      <p>gia tri cua ban da nhap: {{ inputText }}</p>
      <p>Gia tri cua bien: {{ count }}</p>
      <button @click="handleIncrease">increase</button>
      <p>*************** event **************</p>
      <button @click="handleClick('hello')">Click</button>
    </div>
    <div>
      <h3>event</h3>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const image =
  "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS5HzKGA8_RzCPJiVB0LJiLXKMPq1mQXVvrKg&s";
const isVif = true;
const isVshow = true;
const students = [
  {
    id: 1,
    name: "Doan",
    age: 22,
  },
  {
    id: 2,
    name: "Hung",
    age: 19,
  },
  {
    id: 3,
    name: "Tu",
    age: 20,
  },
  {
    id: 4,
    name: "Bla",
    age: 21,
  },
];
const inputText = defineModel();
const count = ref(0);

const handleIncrease = () => {
  count.value++;
};

const handleClick = (mess) => {
  console.log(mess);
};
</script>

<style scoped></style>
