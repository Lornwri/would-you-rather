<script setup>
import { ref } from 'vue'


//Define data
defineProps({
 question: String,
 answer1: String,
 answer2: String,
})

const choice = ref('')

</script>

<template>
 
  <h2>Make your choice!</h2>
  
  {{question}}
  
  <br>
  <br>
  
  <!--Create buttons for answers using HTML value -->
  <input v-model="choice" v-bind:value="answer1" type="radio" id="answer-1">
  <label for="answer-1">{{answer1}}</label>
  
  <input v-model="choice" v-bind:value="answer2" type="radio" id="answer-2">
  <label for="answer-2">{{answer2}}</label>
  
  
</template>

<style scoped>



</style>
