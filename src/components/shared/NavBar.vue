<!-- eslint -->
<template>
  <div id="app">
    <span
      class="mobToggle"
      :class="{ active: showMobileMenu }"
      @click="showMobileMenu = !showMobileMenu"
    >
      <span></span>
      <span></span>
      <span></span>
    </span>

    <ul class="mob_v menu">
      <li>
        <a
          href="#"
          class="_sub"
          :class="{ active: activeId == 'link-1' }"
          @click.prevent="activeLink('link-1')"
          >My Schedule
          <img
            src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png"
        /></a>
        <ul>
          <li class="menu_title">
            My Schedule & Bidding
            <span class="close_btn" @click.prevent="activeLink('link-1')"
              ><img
                src="https://img.icons8.com/material-outlined/24/000000/delete-sign.png"
            /></span>
          </li>
          <li><a href="#">Sub Menu Item</a></li>
          <li><a href="#">Sub Menu Item</a></li>
          <li><a href="#">Sub Menu Item</a></li>
        </ul>
      </li>

      <li>
        <a
          href="#"
          class="_sub"
          :class="{ active: activeId == 'link-2' }"
          @click.prevent="activeLink('link-2')"
          >Safety
          <img
            src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png"
        /></a>

        <ul>
          <li class="menu_title">
            Safety
            <span class="close_btn" @click.prevent="activeLink('link-2')"
              ><img
                src="https://img.icons8.com/material-outlined/24/000000/delete-sign.png"
            /></span>
          </li>
          <li>
            <a
              href="#"
              class="accordion-toggle"
              :class="{ active: activesubId == 'link-3' }"
              >Reporting
              <span @click.prevent="activesubLink('link-3')"
                ><img
                  src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png" /></span
            ></a>
            <ul class="accordion-collapsed">
              <li><a href="#">I-21 Injury Reporting</a></li>
              <li><a href="#">ASAP Reporting</a></li>
              <li><a href="#">General ASAP Information</a></li>
              <li><a href="#">Flight Attendant Incident Report</a></li>
            </ul>
          </li>
          <li>
            <a
              href="#"
              class="accordion-toggle"
              :class="{ active: activesubId == 'link-4' }"
              >Agriculture and Custom
              <span @click.prevent="activesubLink('link-4')"
                ><img
                  src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png" /></span
            ></a>
            <ul class="accordion-collapsed">
              <li>
                <a href="#">Sub Sub Menu Item</a>
              </li>
              <li>
                <a href="#">Sub Sub Menu Item</a>
              </li>
              <li>
                <a href="#">Sub Sub Menu Item</a>
              </li>
            </ul>
          </li>
          <li><a href="#">Known Crewmember</a></li>
          <li><a href="#">Product Safety Data Search</a></li>
        </ul>
      </li>

      <li>
        <a href="#">Training</a>
      </li>

      <li>
        <a
          href="#"
          class="_sub"
          :class="{ active: activeId == 'link-5' }"
          @click.prevent="activeLink('link-5')"
          >Administration
          <img
            src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png"
        /></a>
        <ul>
          <li class="menu_title">
            Administration
            <span class="close_btn" @click.prevent="activeLink('link-5')"
              ><img
                src="https://img.icons8.com/material-outlined/24/000000/delete-sign.png"
            /></span>
          </li>
          <li><a href="#">OJI and Leaves</a></li>
          <li><a href="#">Pay and Benefits</a></li>
          <li><a href="#">Performance</a></li>
          <li><a href="#">Inflight Resource Directory</a></li>
          <li><a href="#">Mobile and Web</a></li>
          <li><a href="#">AFA</a></li>
        </ul>
      </li>

      <li>
        <a
          href="#"
          class="_sub"
          :class="{ active: activeId == 'link-6' }"
          @click.prevent="activeLink('link-6')"
          >Catering Brand
          <img
            src="https://img.icons8.com/external-those-icons-lineal-those-icons/24/000000/external-right-arrows-those-icons-lineal-those-icons-1.png"
        /></a>
        <ul>
          <li class="menu_title">
            Catering Brand
            <span class="close_btn" @click.prevent="activeLink('link-6')"
              ><img
                src="https://img.icons8.com/material-outlined/24/000000/delete-sign.png"
            /></span>
          </li>
          <li><a href="#">Sub Menu Item</a></li>
          <li><a href="#">Sub Menu Item</a></li>
          <li><a href="#">Sub Menu Item</a></li>
        </ul>
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
      showMobileMenu: false,
      activeId: null,
      activesubId: null,
    };
  },
  methods: {
    activeLink(linkIdent) {
      return (this.activeId = this.activeId === linkIdent ? null : linkIdent);
    },
    activesubLink(linkIdent) {
      this.activesubId = this.activesubId === linkIdent ? null : linkIdent;
    },
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

.menu li ul li a:hover {
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

@media only screen and (min-width: 768px) {
  .menu a._sub img {
    display: inline-block !important;
    filter: invert(1);
    transform: rotate(90deg) translateX(1px) translateY(-4px);
    width: 15px;
    margin-top: -1px;
  }
  .menu a img {
    display: none !important;
  }

  li.menu_title {
    display: none !important;
  }
  .menu li ul ul {
    position: relative !important;
    top: 0 !important;
  }
  ._sub + ul {
    max-height: 0 !important;
    overflow: hidden;
    transition: 0.6s;
  }
  ._sub.active + ul {
    max-height: 10000px !important;
  }
}

@media only screen and (max-width: 767px) {
  .mobToggle {
    position: relative;
    width: 32px;
    height: 30px;
    cursor: pointer;
    display: inline-block;
  }
  .mobToggle:hover span {
    background: #999;
  }
  .mobToggle span {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 2px;
    transition: all 0.2s, background 0s;
    background: #999;
  }
  .mobToggle span:nth-child(2) {
    top: 6px;
  }
  .mobToggle span:last-child {
    top: 12px;
  }

  .mobToggle.active span:first-child,
  .mobToggle.active span:last-child {
    top: 8px;
  }
  .mobToggle.active span:first-child {
    transform: rotate(45deg);
  }
  .mobToggle.active span:last-child {
    transform: rotate(-45deg);
  }
  .mobToggle.active span:nth-child(2) {
    opacity: 0;
    visibility: hidden;
  }

  .mobToggle + .menu {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 35px;
    left: -200%;
    transition: 0.4s;
    display: block;
  }

  .mobToggle.active + .menu {
    left: 0;
  }

  .mobToggle + .menu li {
    width: 100%;
    text-align: left;
    text-transform: uppercase;
  }

  ._sub img {
    width: 24px;
    filter: invert(1);
    position: absolute;
    right: 0;
    top: 0;
    padding: 19px;
    background: #6a01013d;
  }

  .mobToggle + .menu li a {
    border-bottom: 1px solid #376e91;
  }

  .menu li a._sub.active + ul {
    right: 0px;
  }

  .menu li a._sub + ul {
    position: fixed;
    top: 35px;
    height: 100% !important;
    background: #5193c7;
    right: -200%;
    transition: 0.4s;
    left: auto !important;
    width: 85%;
    z-index: 99;
  }

  li.menu_title {
    background: #76b3e3 !important;
    padding: 20px;
  }

  ul.accordion-collapsed {
    position: relative !important;
    top: 0 !important;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.6s ease;
  }

  a.accordion-toggle.active + ul {
    max-height: 1000px;
  }

  .accordion-toggle span {
    padding: 18px;
    position: absolute;
    right: 0;
    top: 0;
    transition: 0.3s;
  }

  .accordion-toggle.active span {
    transform: rotate(90deg);
  }

  ul.accordion-collapsed a {
    background: #6dacdd;
    border-color: #5393c5 !important;
  }

  ._sub + ul li:hover,
  ._sub + ul li:focus,
  ._sub + ul li:active {
    background: transparent !important;
  }

  span.close_btn {
    position: absolute;
    right: 0px;
    padding: 16px 15px 15px;
    top: 0;
    background: #64a0cf;
  }

  span.close_btn img {
    transform: translateY(4px);
    filter: invert(1);
  }

  .accordion-toggle span img {
    width: 24px;
    transform: translateY(1px);
    filter: invert(1);
  }

  li.menu_title {
    box-sizing: border-box;
  }
}
</style>
