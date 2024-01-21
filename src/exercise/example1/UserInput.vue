<template>
  <h1>{{ message }}</h1>

  <!--
    Bind to a method/function.
    The @click syntax is short for v-on:click.
  -->
  <el-button type="primary" @click="reverseMessage">Reverse Message</el-button>

  <!-- Can also be an inline expression statement -->
  <el-button @click="message += '!'">Append "!"</el-button>

  <!--
    Vue also provides modifiers for common tasks
    such as e.preventDefault() and e.stopPropagation()
  -->
  <a href="https://vuejs.org" @click.prevent="notify">
    A link with e.preventDefault()
  </a>
</template>
<script setup>
import {ref} from "vue";
import {ElMessage} from "element-plus";

const message = ref("Hello, Vue 3!");

function reverseMessage() {
  message.value = message.value.split("").reverse().join("");
}

function notify() {
  ElMessage({
    message: 'Congrats, this is a success message.',
    type: 'warn',
  })
}
</script>

<style scoped>

</style>