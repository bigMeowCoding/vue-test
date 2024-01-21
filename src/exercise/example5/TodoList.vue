<script setup lang="ts">
import {ref} from 'vue'
import TodoItem from "./TodoItem.vue";

const groceryList = ref([
  {id: 0, text: 'Vegetables'},
  {id: 1, text: 'Cheese'},
  {id: 2, text: 'Whatever else humans are supposed to eat'}
])
</script>

<template>
  <ul>
    <TodoItem v-for="item in groceryList"
              :name="item.text"
              :key="item.id"
    ></TodoItem>
  </ul>
</template>

<style scoped>

</style>