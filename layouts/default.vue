<template>
  <Header />
  <main class="layout-main">
    <slot />
  </main>
</template>
<style lang="scss">
html,
body {
  width: 100%;
  height: 100%;

  #__nuxt {
    width: 100%;
    height: 100%;
    /* background: linear-gradient(90deg, #ffd700 65%, #00008b 35%); */
    background: #dcdcdc;

    .layout-main {
    }
  }
}
</style>
