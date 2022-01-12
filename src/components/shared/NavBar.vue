<template>
  <div id="app">
    <ul class="menu">
      <li @mouseover="listOne = true" @mouseleave="listOne = false">
        <a href="#">My Schedule & Bidding</a>

        <transition name="fade">
          <ul v-if="listOne" @click="listOne = false">
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
          </ul>
        </transition>
      </li>

      <li @mouseover="listTwo = true" @mouseleave="listTwo = false">
        <a href="#">Safety</a>

        <transition name="fade">
          <ul v-if="listTwo" @click="listTwo = false">
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
          </ul>
        </transition>
      </li>

      <li>
        <a href="#">Training</a>
      </li>

      <li @mouseover="listThree = true" @mouseleave="listThree = false">
        <a href="#">Administration</a>

        <transition name="fade">
          <ul v-if="listThree" @click="listThree = false">
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
          </ul>
        </transition>
      </li>

      <li @mouseover="listFour = true" @mouseleave="listFour = false">
        <a href="#">Catering Brand</a>

        <transition name="fade">
          <ul v-if="listFour" @click="listFour = false">
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
            <li><a href="#">Sub Menu Item</a></li>
          </ul>
        </transition>
      </li>

      <li>
        <a href="#">Hotles</a>
      </li>

      <li>
        <a href="#">My Base</a>
      </li>

      <li>
        <a href="#">Recognition</a>
      </li>

      <li>
        <a href="#">Leadership Team</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "NavBar",

  data() {
    return {
      listOne: false,
      listTwo: false,
      listThree: false,
      listFour: false,
    };
  },
};
</script>

<style scoped>
.menu {
  font: 14px/1.5 "Open Sans", sans-serif;
  font-weight: 600;
  margin: 0;
  padding: 0;
  text-align: center;
  list-style: none;
}

.menu a {
  display: block;
  padding: 20px;
  color: #fff;
  text-decoration: none;
}

.menu li {
  display: block;
  float: left;
  position: relative;
  background: #01426a;
  color: #fff;
  min-width: 180px;
}

.menu li ul {
  position: absolute;
  left: 0;
  top: 61px;
  margin: 0;
  padding: 0;
}

.menu li ul li {
  background: #5193c7;
  transition: background 0.2s;
}

.menu li ul li:hover {
  background: #444;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>
