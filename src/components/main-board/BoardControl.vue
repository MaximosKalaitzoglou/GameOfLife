<template>
  <div id="board-control">
    <div class="button-group">
      <button class="btn first" v-if="!isRunning" @click="$emit('welcome')">
        Start
      </button>
      <button class="btn first" v-if="isRunning" @click="$emit('stop')">
        Stop
      </button>

      <button class="btn first" @click="$emit('reset')" :disabled="isRunning">
        Reset
      </button>
      <button
        class="btn first"
        @click="$emit('randomize')"
        :disabled="isRunning"
      >
        Randomize
      </button>
      <span
        >Generation: <span class="emphasis">{{ generation }}</span></span
      >
      <span
        >Cells Alive: <span class="emphasis">{{ cellsAlive }}</span></span
      >
    </div>
  </div>
</template>

<script>
export default {
  emit: ["welcome"],
  props: ["generation", "isRunning", "cellsAlive"],
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
  .button-group {
    background-color: black;
    border-radius: 1rem;
    width: 900px;
  }
  span {
    font-size: 1em;
    font-weight: 500;

    text-transform: uppercase;
    line-height: 1;
    color: #fff;
    padding-top: 2rem;
    padding-left: 1rem;
    font-family: "Roboto", sans-serif;
    transition: all 0.3s ease;
    .emphasis {
      color: #f95959;
      font-weight: 700;
    }
  }
  // Basic Button Style
  .btn {
    box-sizing: border-box;
    appearance: none;
    background-color: transparent;
    border: 2px solid $secondary-color;
    border-radius: 0.6em;
    color: $secondary-color;
    cursor: pointer;
    display: flex;
    align-self: center;
    font-size: 1em;
    font-weight: 400;
    line-height: 1;
    margin: 10px;
    padding: 0.5em 0.8em;
    text-decoration: none;
    text-align: center;
    text-transform: uppercase;
    font-family: "Montserrat", sans-serif;
    font-weight: 700;

    &:hover,
    &:focus {
      color: #fff;
      outline: 0;
    }
    &:disabled {
      outline: none;
      color: #333;
      background-color: rgb(141, 141, 141);
      // border: none;

      &:hover {
        outline: 0;
        box-shadow: none;
      }
    }
  }

  //BUTTON 1
  .first {
    transition: all 300ms ease-in-out;
    &:hover {
      box-shadow: 0 0 40px 40px $secondary-color inset;
    }
  }
}
</style>
