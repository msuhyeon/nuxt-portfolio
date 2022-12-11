<template>
  <div class="nav">
    <ul class="nav__list">
      <li class="nav__item">
        <NuxtLink class="nav__link" :to="{ path: '/' }" @click="clickNavItem"
          >HOME</NuxtLink
        >
      </li>
      <li class="nav__item">
        <NuxtLink
          class="nav__link"
          :to="{ path: '/about' }"
          @click="clickNavItem"
          >ABOUT</NuxtLink
        >
      </li>
      <li class="nav__item">
        <NuxtLink
          class="nav__link"
          :to="{ path: '/projects' }"
          @click="clickNavItem"
          >PROJECTS</NuxtLink
        >
      </li>
      <li class="nav__item">
        <NuxtLink
          class="nav__link"
          :to="{ path: '/contact' }"
          @click="clickNavItem"
          >CONTACT</NuxtLink
        >
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Navigation',
  methods: {
    clickNavItem() {
      this.$emit('isClosingNav', true);
    },
  },
};
</script>
