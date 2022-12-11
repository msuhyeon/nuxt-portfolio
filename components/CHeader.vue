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

      <button
        type="button"
        class="menu__btn--toggle"
        @click="
          () => {
            isShowNav = !isShowNav;
          }
        "
      />
    </div>
    <Navigation v-if="isShowNav" @isClosingNav="isClosingNav" />
  </header>
</template>
<script>
import Navigation from './Navigation.vue';
export default {
  name: 'CHeader',
  data() {
    return {
      isShowNav: false,
    };
  },
  methods: {
    handleToggleClick() {
      this.isShowNav = true;
    },
    isClosingNav(data) {
      this.isShowNav = !data;
    },
    bodyClickEvent() {
      document.body.onclick = function (e) {
        const event = e || window.event;

        document.body.innerHTML = '';
      };
    },
  },
  components: { Navigation },
};
</script>
<style lang="scss" scope>
.header {
  position: relative;
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

    .menu__btn--toggle {
      position: relative;
      display: inline-flex;
      width: 2.78em;
      height: 2.09em;
      margin-top: 0.699em;
      background: none;
      color: #00008b;
      z-index: 999;
      border: none;
      cursor: pointer;

      &::before,
      &::after {
        content: '';
        position: absolute;
        width: 100%;
        height: 2px;
        background: currentColor;
        transition: 0.2s ease;
        transform: rotate(0deg);
      }
      &::before {
        top: 0;
        right: 0;
      }
      &::after {
        top: 1.13em;
        right: 0;
      }
    }
  }
  .nav {
    position: absolute;
    right: 0;
    background: #fff;
    width: 25rem;
    height: 40rem;

    .nav__list {
      display: flex;
      flex-direction: column;
      padding: 2.8rem 2rem;

      .nav__item {
        font-size: 2rem;
        margin-bottom: 3.5rem;
        cursor: pointer;

        .nav__link {
          color: #000;
        }
      }
    }
  }
}
</style>
