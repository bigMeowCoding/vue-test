<script>
export default {
  data() {
    return { name: "lilei", age: 18 };
  },
  methods: {
    // 求和
    sum(a, b) {
      return a + b;
    },
  },
};
</script>

<template>
  <div class="flex justify-center">
    <div class="bg-red">red</div>
    <div class="bg-yellow">yellow</div>
  </div>
  <div>{{ name }}</div>
  <div>
    {{ age }}
  </div>
  <!-- <el-button>button</el-button> -->
</template>
<style scoped></style>
