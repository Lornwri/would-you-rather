<script setup>
import WouldYouRather from './components/WouldYouRather.vue'

import {ref} from 'vue'

//Data for 'wyr' question and answers
const wyrQuestion = ref('The aliens that make first contact be robotic or organic?')
const wyrAnswer1 = ref('Organic')
const wyrAnswer2 = ref('Robotic')


//stores user's answer selection

const userSelection = ref('') //empty string for user's answer

function updateUserSelection(userChoice) {
  userSelection.value = 'Thanks! You chose ${userChoice}'
}

</script>

<template>
  
  <div id="app">
  
  <h1>Would You Rather</h1>
  
  <WouldYouRather 
      v-bind:question="wyrQuestion" 
      v-bind:answer1="wyrAnswer1" 
      v-bind:answer2="wyrAnswer2">
      v-on:answer-selected="updateUserSelection">
  </WouldYouRather>
  
  {{ userSelection }}
    
  </div>

</template>

<style scoped>

#app {
  text-align: center;
  font-family: 'Courier New', Courier, monospace;
  font-size: 1.5em;
  color: #000000;
  background-color: #ffffff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

</style>
