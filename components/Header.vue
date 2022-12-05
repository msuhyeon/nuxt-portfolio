<template>
  <header class="header">
    <div class="header__inner">
      <NuxtLink to="/" class="header__logo">
        <img
          class="header__logo--img"
          src="../assets/images/Avatar.png"
          alt="avatar image"
        />
        <h2 class="header__logo--sub">Maeng SuHyeon</h2>
      </NuxtLink>
      <div class="nav">
        <ul class="nav__list">
          <li class="nav__item">
            <NuxtLink class="nav__link" :to="{ path: '/' }">HOME</NuxtLink>
          </li>
          <li class="nav__item">
            <NuxtLink class="nav__link" :to="{ path: '/about' }"
              >ABOUT</NuxtLink
            >
          </li>
          <li class="nav__item">
            <NuxtLink class="nav__link" :to="{ path: '/projects' }"
              >PROJECTS</NuxtLink
            >
          </li>
          <li class="nav__item">
            <NuxtLink class="nav__link" :to="{ path: '/contact' }"
              >CONTACT</NuxtLink
            >
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>
<script>
export default defineComponent({
  setup() {},
});
</script>
<style lang="scss" scope>
.header {
  background: #fff;

  .header__inner {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 5rem;

    .header__logo {
      display: flex;
      align-items: center;

      .header__logo--img {
        width: 5rem;
        height: 5rem;
      }

      .header__logo--sub {
        color: #ffd700;
        font-size: 2rem;
      }
    }
  }
  .nav {
    .nav__list {
      display: flex;
      align-items: center;

      .nav__item {
        font-size: 2rem;
        margin-right: 2rem;
        cursor: pointer;

        .nav__link {
          color: #000;
        }
      }
    }
  }
}
</style>
