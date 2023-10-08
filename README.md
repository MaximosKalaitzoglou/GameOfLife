# John Conway's Game of Life
This is my implementation of the popular cellular automaton known as **Game of Life** using Vue Js. 
<br/>
<br />
You can try it out on my github page [Game of Life](https://maximoskalaitzoglou.github.io/GameOfLife)

## What is the Game of Life 
The Game of Life is a cellular automaton, and was invented by [John Conway](https://en.wikipedia.org/wiki/John_Horton_Conway).

## Rules
  1. Any live cell with fewer than two live neighbours dies, as if by underpopulation.
  2. Any live cell with two or three live neighbours lives on to the next generation.
  3. Any live cell with more than three live neighbours dies, as if by overpopulation.
  4. Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

These rules, which compare the behaviour of the automaton to real life, can be condensed into the following:

  1. Any live cell with two or three live neighbours survives.
  2. Any dead cell with three live neighbours becomes a live cell.
  3. All other live cells die in the next generation. Similarly, all other dead cells stay dead.
