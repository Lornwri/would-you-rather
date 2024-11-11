<script setup>
import WouldYouRather from './components/WouldYouRather.vue'

import {ref} from 'vue'

const wyrQuestion = ref('The aliens that make first contact be robotic or organic?')
const wyrAnswer1 = ref('Organic')
const wyrAnswer2 = ref('Robotic')

//stores user's answers

const userSelection = ref('') //empty string for user's answer

</script>

<template>
  
  <h1>Would You Rather?</h1>
  
  <WouldYouRather v-bind:question="wyrQuestion" 
                  v-bind:answer1="wyrAnswer1" 
                  v-bind:answer2="wyrAnswer2">
  </WouldYouRather>

</template>

<style scoped>

</style>
