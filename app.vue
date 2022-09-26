<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
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
</style>
