<script setup lang="ts">
const props = defineProps({
  name: {
    type: String,
    required: true,
    default: 'default name'
  },
})
</script>

<template>

  <li>
    {{ name }}
  </li>
</template>

<style scoped>

</style>