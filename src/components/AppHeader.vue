<template>
  <h4 class="title">Welcome to <span class="title-emphasis">The Game of Life</span></h4>
</template>

<script>
export default {
  setup() {},
};
</script>

<style scoped lang="scss">
$title-color: #6a5acd;
.title {
  font-family: "Times New Roman", Times, serif;
  color: #333;
  font-size: 1.2rem;
  .title-emphasis {
    color: $title-color;
  }
}
</style>
