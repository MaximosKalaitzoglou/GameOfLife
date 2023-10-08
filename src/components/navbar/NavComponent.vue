<template>
  <div id="container">
    <div id="navigation-bar">
      <nav>
        <ul>
          <!-- <li><img src="../../assets/logo.png" alt="" />ue Js</li> -->
          <li>The Game of Life</li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">
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
  i {
    height: 50px;
    width: 50px;
  }
  ul {
    text-align: start;
    list-style-type: none;
    list-style-type: none;
    margin: 0;
    padding: 15px;
    li {
      display: inline;
      font-size: 1.7rem;
      color: $font-color;
      margin-right: 2rem;
    }
  }
}

// .myBtn {
//   padding: 0.4rem 2.2rem !important;
//   // margin: 2%;
//   font-size: 1rem;
//   position: relative;
//   top: -0.2rem;
//   cursor: pointer;
//   color: #333;
//   font-weight: 600;
//   border: 2px solid #333;
//   background-color: white;
//   border-radius: 5px;
//   transition: all 0.3s ease;
// }

// .myBtn:hover {
//   color: $font-color;
//   background-color: $secondary-color;
//   border: 2px solid $background-color-nav;
// }

.content {
  text-align: center;
}
</style>
