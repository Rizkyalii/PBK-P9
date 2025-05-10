<script setup>
import { ref } from 'vue';
import ChildComp from './childcamp.vue';

const msg = ref('from parent');

</script>
<template>
  <!-- Component -->
   <ChildComp />



  <!-- Slots -->
  <ChildComp>Message:{{ msg }}</ChildComp>
</template>