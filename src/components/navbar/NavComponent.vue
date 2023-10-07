<template>
  <div id="container">
    <div id="navigation-bar">
      <nav>
        <ul>
          <li><img src="../../assets/logo.png" alt="" />ue Js</li>
          <li>The Game of Life</li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">

@import url("https://fonts.googleapis.com/css?family=Fira+Sans");

$background-color-nav: #233142;
$font-color: #e3e3e3;
$secondary-color: #f95959;

#container {
  width: 100%;
  display: inline-block;
}

/** HEADER */

/** NAVIGATION BAR */
nav {
  overflow: hidden;
  background-color: $background-color-nav;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  img {
    width: 20px;
    height: 20px;
    padding: 0;
    margin: 0;
  }
  ul {
    text-align: start;
    list-style-type: none;
    list-style-type: none;
    margin: 0;
    padding: 15px;
    li {
      display: inline;
      font-family: "Fira Sans", sans-serif;
      font-size: 1rem;
      color: $font-color;
      margin-right: 2rem;
    }
  }
}

.content {
  text-align: center;
}
</style>
