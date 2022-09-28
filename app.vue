<template>
  <SharedHeader />
  <NuxtPage />
  <SharedFooter />
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  color: inherit;
  text-decoration: none;
}
#__nuxt {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background: #EBEFF0;
}
#__nuxt > main {
  flex-grow: 1;
}
/* hide scrollbar but allow scrolling */
body {
  -ms-overflow-style: none; /* for Internet Explorer, Edge */
  scrollbar-width: none; /* for Firefox */
  overflow-y: scroll;
}

body::-webkit-scrollbar {
  display: none; /* for Chrome, Safari, and Opera */
}
</style>
