<template>
  <header :class="stateMenu">
    <div class="menu">
      <div class="ico-menu" @click="toggleMenu()">
        <i class="ico-menu-square ico-menu-square-1"></i>
        <i class="ico-menu-square ico-menu-square-2"></i>
        <i class="ico-menu-square ico-menu-square-3"></i>
        <i class="ico-menu-square ico-menu-square-4"></i>
        <i class="ico-menu-square ico-menu-square-5"></i>
        <i class="ico-menu-square ico-menu-square-6"></i>
        <i class="ico-menu-square ico-menu-square-7"></i>
        <i class="ico-menu-square ico-menu-square-8"></i>
        <i class="ico-menu-square ico-menu-square-9"></i>
      </div>
      <img src="~/assets/img/papillon_menu.svg" alt="" srcset="">
    </div>
  </header>
  <div class="content" v-if="stateMenu">
    <nav>
      <nuxt-link :to="{ name: 'index' }" @click="toggleMenu()">Mes services</nuxt-link>
      <nuxt-link :to="{ name: 'realisations' }" @click="toggleMenu()">Réalisation</nuxt-link>
      <nuxt-link :to="{ name: 'contact' }" @click="toggleMenu()">Contact</nuxt-link>
    </nav>
    <div>
      AAAAAAAAA
    </div>
  </div>
</template>

<script>
import Header from "../home/Header";
export default {
  components: {Header},
  data() {
    return {
      stateMenu: null
    }
  },
  methods: {
    toggleMenu() {
      const body = document.body;
      this.stateMenu = this.stateMenu? null : 'active'
      body.style.position = this.stateMenu? 'fixed' : ''
    }
  }
}
</script>

<style lang="scss" scoped>
header {
  position: absolute;
  width: 100%;
  padding: 20px;
  border-bottom: 3px solid transparent;
  z-index: 2;
  position: fixed;
}
header:not(.active) {
  border-bottom:  3px solid gray;
  position: inherit;
}
.menu {
  display: flex;
  justify-content: space-between;
  max-width: 1350px;
  margin: auto;
  z-index: 5;
}
.ico-menu {
  position: relative;
  height: 30px;
  width: 30px;
  cursor: pointer;
  &-square {
    position: absolute;
    height: 8px;
    width: 8px;
    background-color: #717FFF;
    transition-duration: 0.25s;
    &-1 {
      top: 0;
      left: 0;
    }
    &-2 {
      top: 0;
      left: 11px;
    }
    &-3 {
      top: 0;
      left: 22px;
    }
    &-4 {
      top: 11px;
      left: 0;
    }
    &-5 {
      top: 11px;
      left: 11px;
    }
    &-6 {
      top: 11px;
      left: 22px;
    }
    &-7 {
      top: 22px;
      left: 0;
    }
    &-8 {
      top: 22px;
      left: 11px;
    }
    &-9 {
      top: 22px;
      left: 22px;
    }
  }
}

header.active {
  .ico-menu .ico-menu-square {
    top: 11px;
    left: 11px;
    &-1 {
      animation: topLeft 0.5s forwards;
    }
    &-3 {
      animation: topRight 0.5s forwards;
    }
    &-7 {
      animation: bottomLeft 0.5s forwards;
    }
    &-9 {
      animation: bottomRight 0.5s forwards;
    }
  }
}

@keyframes bottomRight {
  0%   {

  }
  50%  {
    top: 11px;
    left: 11px;
  }
  100% {
    top: 22px;
    left: 22px;
  }
}

@keyframes topRight {
  0%   {

  }
  50%  {
    top: 11px;
    left: 11px;
  }
  100% {
    top: 0;
    left: 22px;
  }
}

@keyframes bottomLeft {
  0%   {

  }
  50%  {
    top: 11px;
    left: 11px;
  }
  100% {
    top: 22px;
    left: 0;
  }
}

@keyframes topLeft {
  0%   {

  }
  50%  {
    top: 11px;
    left: 11px;
  }
  100% {
    top: 0;
    left: 0;
  }
}




.content {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  z-index: 1;
  background: transparent radial-gradient(closest-side at 59% 54%, #1A1D31 0%, #060710 100%) 0% 0% no-repeat padding-box;
}
nav {
  max-width: 1500px;
  margin: auto;
  color: white;
  font-size: 80px;
  display: flex;
  gap: 1em;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  border-left: 3px solid gray;
  padding: 0 70px;
}
nav a {
  width: min-content;
  white-space: nowrap;
}
nav a:hover {
  color: #717FFF;
}
</style>
