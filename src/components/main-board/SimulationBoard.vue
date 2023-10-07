<template>
  <board-control @welcome="runGame" @randomize="randomizeBoard"></board-control>

  <div class="board">
    <div class="grid" id="myGrid">
      <div
        class="grid-item"
        style="--aspect-ratio: 1/1"
        :style="
          this.board[i] === true
            ? 'background-color: #f95959;'
            : 'background-color: black;'
        "
        v-for="i in 1200"
        :key="'cell' + i"
      ></div>
    </div>
  </div>
</template>

<script>
import BoardControl from "./BoardControl.vue";

export default {
  components: {
    BoardControl,
  },

  setup() {},
  data() {
    return {
      bgColorActive: "#f95959",
      bgColorInactive: "black",
      rows: 30,
      columns: 40,
      board: null,
      gameState: "inactive",
    };
  },

  methods: {
    markCell: function (event) {
      //   console.log(event.target.style.backgroundColor);
      if (event.target.style.backgroundColor === this.bgColorActive) {
        event.target.style.backgroundColor = this.bgColorInactive;
      } else {
        event.target.style.backgroundColor = this.bgColorActive;
      }
    },

    randomizeBoard() {
      for (let i = 0; i < this.rows * this.columns + 1; i++) {
        this.board[i] = Math.random(0, 1) < 0.5 ? true : false;
      }
    },

    makeBoard() {
      let board = [];
      for (let i = 0; i < this.rows * this.columns + 1; i++) {
        board[i] = false;
      }
      return board;
    },

    findNeighbours(currCell) {
      let neighbours = 0;
      const directions = [
        -1,
        this.columns,
        -this.columns,
        1,
        this.columns - 1,
        this.columns + 1,
        -this.columns - 1,
        -this.columns + 1,
      ];
      for (const d in directions) {
        let newX = currCell + d;
        if (newX >= 0 && newX <= 1200 && this.board[newX]) {
          neighbours++;
        }
      }
      return neighbours;
    },

    runGame() {
      for (let i = 0; i < this.rows * this.columns + 1; i++) {
        let n = this.findNeighbours(i);
        if (this.board[i]) {
          if (n === 2 || n === 3) {
            this.board[i] = true;
          } else {
            this.board[i] = false;
          }
        } else {
          if (!this.board[i] && n === 3) {
            this.board[i] = true;
          }
        }
      }
      // window.setTimeout(() => {
      //   this.runGame();
      // }, 100);
    },
  },
  created() {
    this.board = this.makeBoard();
  },
};
</script>

<style lang="scss" scoped>
$background-color-nav: #233142;
$font-color: #e3e3e3;
$secondary-color: #f95959;

.grid {
  display: grid;
  width: 800px;
  height: 600px;
  grid-template-rows: repeat(30, 20px);
  grid-template-columns: repeat(40, 20px);
  margin: 10rem auto;
  background-color: #e4c6c6;
  .grid-item {
    width: 20px;
    height: 20px;
    border: 1px solid #333;
  }
}

/** HEADER */
</style>
