<script setup>
import {ref} from 'vue'

import WouldYouRather from './components/WouldYouRather.vue'

//Data for 'wyr' question and answers
const wyrQuestion = ref('The aliens that make first contact be robotic or organic?')
const wyrAnswer1 = ref('Organic')
const wyrAnswer2 = ref('Robotic')


//stores user's answer selection

const userSelection = ref('') //empty string for user's answer

//Update user's selections
function updateUserSelection(userChoice) {
  userSelection.value = `Thanks! You chose ${userChoice}`
}

</script>

<template>
  
  <div id="app">
  
  <h1>Would You Rather</h1>
  
    <!--passing props to WouldYouRather component-->
  <WouldYouRather 
      v-bind:question="wyrQuestion" 
      v-bind:answer1="wyrAnswer1" 
      v-bind:answer2="wyrAnswer2"
      v-on:answer-selected="updateUserSelection"
  >
  </WouldYouRather>
  
  {{ userSelection }}
    
  </div>

</template>

<style scoped>

#app
{
  text-align: center;
  margin-top: 60px;
}
</style>
