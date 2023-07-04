<template>
  <div class="navbar coffee-container">
    <div class="navbar__logo">Coffee <span>Factory</span></div>

    <a class="navbar__open" @click="showMobileMenu = !showMobileMenu">
      <i class="iconify" data-icon="ic:round-menu" />
    </a>

    <div
      class="navbar__content"
      :class="{
        'navbar__content--open': showMobileMenu,
        'navbar__content--closed': !showMobileMenu,
      }"
    >
      <a class="navbar__close" @click="showMobileMenu = !showMobileMenu">
        <i class="iconify" data-icon="ic:round-close" />
      </a>

      <ul class="navbar__menu">
        <li
          v-for="(link, index) in menuLinks"
          :key="`link-${index}`"
          class="navbar__item"
        >
          <a
            :href="link.href"
            class="navbar__link"
            @click="showMobileMenu = false"
            >{{ link.name }}</a
          >
        </li>
      </ul>

      <div class="navbar__cart">
        <i class="iconify" data-icon="mdi-cart-outline" />
        <span class="navbar__counter"></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "navbar",

  data() {
    return {
      showMobileMenu: false,
      menuLinks: [
        { name: "Home", href: "#" },
        { name: "About", href: "#about" },
        { name: "Trending", href: "#trending" },
        { name: "Delivery", href: "#delivery" },
        { name: "Contact", href: "#contact" },
      ],
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu;
    },
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 20px;
  padding-bottom: 20px;

  @media (max-width: 980px) {
    flex-wrap: wrap;
  }

  &__logo {
    font-size: 40px;
    font-weight: 900;

    span {
      color: var(--primary-color);
    }
  }

  &__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 1;

    @media (max-width: 980px) {
      flex-direction: column;
      flex-basis: 100%;
      position: fixed;
      top: 0;
      right: 0;
      background-color: var(--primary-color);
      width: 100%;
      height: 100%;
      justify-content: start;
      gap: 20px;

      &--open {
        display: flex;
      }
      &--closed {
        display: none;
      }
    }
  }

  &__menu {
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    margin-right: 60px;
    padding: 0;

    @media (max-width: 980px) {
      flex-direction: column;
      margin-right: 0;
      margin-top: 50px;
      gap: 20px;
    }
  }

  &__item {
    padding: 0 10px;
  }

  &__link {
    font-size: 18px;
    color: var(--secondary-color);
    font-weight: 500;

    @media (max-width: 980px) {
      font-size: 26px;
      color: #fff;
    }
  }

  &__cart {
    position: relative;

    svg {
      font-size: 30px;

      @media (max-width: 980px) {
        color: #fff;
      }
    }
  }

  &__counter {
    padding: 5px;
    border-radius: 50%;
    background-color: #cf7138;
    color: #fff;
    position: absolute;
    right: -2px;
    top: 0;
  }

  &__open {
    display: none;

    @media (max-width: 980px) {
      display: flex;
      margin-top: 5px;
    }

    svg {
      font-size: 40px;
    }
  }

  &__close {
    display: none;
    font-size: 40px;
    position: absolute;
    right: 20px;
    top: 25px;
    color: #fff;

    @media (max-width: 980px) {
      display: flex;
    }
  }
}
</style>