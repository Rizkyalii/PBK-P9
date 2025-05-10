<script setup>
import { ref } from 'vue';
import ChildComp from './childcamp.vue';

// Props
const greeting = ref('Hello from parent')

// Emits
const childMsg = ref('No child msg yet')

// Slots
const msg = ref('from parent');



</script>
<template>
  <!-- Component -->
   <ChildComp />


  <!-- Props -->
  <ChildComp :msg="greeting" />

  <!-- Emits -->
  <ChildComp @response="(msg) => childMsg = msg" />

  <!-- Slots -->
  <ChildComp>Message:{{ msg }}</ChildComp>
</template>