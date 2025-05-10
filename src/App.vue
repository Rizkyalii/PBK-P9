<script setup>
import { ref } from 'vue';
import ChildComp from './childcamp.vue';


// Slots
const msg = ref('from parent');

// Props
const greeting = ref('Hello from parent')

</script>
<template>
  <!-- Component -->
   <ChildComp />


  <!-- Props -->
  <ChildComp :msg="greeting" />

  <!-- Slots -->
  <ChildComp>Message:{{ msg }}</ChildComp>
</template>