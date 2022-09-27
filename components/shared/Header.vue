<template>
  <header>
    <div class="menu">
      <div class="ico-menu">
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
        <i class="ico-menu-square"></i>
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
export default {
  data() {
    return {
      stateMenu: null
    }
  },
  methods: {
    toggleMenu() {
      // const body = document.body;
      this.stateMenu = this.stateMenu? null : 'active'
      // body.style.position = this.stateMenu? 'fixed' : ''
    }
  }
}
</script>

<style scoped>
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
  height: 33px;
  width: 33px;
  display: flex;
  gap: 4px;
  flex-wrap: wrap;
}
.ico-menu-square {
  background-color: #717FFF;
  height: 7px;
  width: 7px;
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
