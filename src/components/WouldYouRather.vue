<script setup>
import { ref } from 'vue'


//Define data
defineProps({
 question: String,
 answer1: String,
 answer2: String,
})

const emit = defineEmits(['answer-selected'])

const choice = ref('')

function choiceMade() {
  emit('answer-selected', choice.value)}

</script>

<template>
 
  <div id="wyr">
    
  <h2>Make your choice!</h2>
    
    <div id="question">
  {{question}}
    </div>
    
    <div id="answers">
  <br>
  <br>
  <!--Create buttons for answers using HTML value -->
  <input v-model="choice" v-bind:value="answer1" type="radio" id="answer-1">
  <label for="answer-1">{{answer1}}</label>
  
  <input v-model="choice" v-bind:value="answer2" type="radio" id="answer-2">
  <label for="answer-2">{{answer2}}</label>
    </div>
    
  </div>
  
</template>

<style scoped>

#wyr {
  background-color: lightcoral;
  padding: 15px;
  width: 500px;
  height: 500px;
  border: 1px solid black;
  border-radius: 10px;
  text-align: center;
  font-size: 20px;
}

#answers {
  padding: 10px;
  background-color: lightcoral;
  border: 2px solid black;
  border-radius: 10px;
  text-align: center;
}
</style>
