<template>
  <div id="board-control">
    <div class="button-group">
      <button @click="$emit('welcome')">Start</button>
      <button>Stop</button>
      <button @click="$emit('randomize')">Randomize</button>
    </div>
  </div>
</template>

<script>
export default {
  emit: ["welcome"],
  setup() {},
};
</script>

<style lang="scss" scoped>
$background-color-nav: #233142;
$font-color: #e3e3e3;
$secondary-color: #f95959;

div {
  position: absolute;
  top: 3rem;
  display: flex;
  background-color: $background-color-nav;
  height: 80px;
  width: 100%;
  margin-bottom: 0;
  justify-content: center;
  button {
    color: #fff;
    // background-color: transparent;
    padding: 0m;
    margin-right: 2rem;
    width: 100px;
    border-radius: 5px;
    outline: none;
    background-color: $secondary-color;
    height: 30px;
    cursor: pointer;
    &:hover {
      background-color: #333;
      color: #fff;
    }
  }
}
</style>
