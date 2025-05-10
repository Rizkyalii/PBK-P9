<!-- Props -->
<script setup>
const props = defineProps({
  msg: String
})

// Emits
const emit = defineEmits(['response'])

emit('response', 'hello from child')
</script>


<template>

    <!-- Component  -->
    <h1>Child Component</h1>

    <!-- Props -->
     <h2>{{ msg || 'No props passed yet' }}</h2>

    <!-- Slots -->
    <slot>Fallback Message</slot>
</template>