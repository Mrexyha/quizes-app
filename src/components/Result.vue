<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";

const { quizQuestionLength, numberOfCorrectAnswers } = defineProps([
  "quizQuestionLength",
  "numberOfCorrectAnswers",
]);
</script>

<template>
  <div class="results">
    <p>Your Results...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink class="go-back-btn" to="/">Go Back</RouterLink>
  </div>
</template>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}

.go-back-btn {
  width: 100px;
  height: 80px;
  background-color: rgb(234, 194, 145);
  padding: 10px 20px;

  text-decoration: none;
  font-size: 20px;
  color: white;

  border-radius: 12px;
}

.go-back-btn:hover {
  background-color: rgb(206, 159, 101);

  font-size: 30px;
}
</style>
