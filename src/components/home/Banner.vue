<template>
  <section class="banner coffee-container">
    <div class="banner__content">
      <h1 class="banner__title">
        Factory<br><span>Iced Coffee</span>
      </h1>
      <p class="banner__description">
        The Factory Frappuccino features extra dark cocoa blended with roasted
        coffee.
      </p>
      <p class="banner__price">
        C$ 12.60
      </p>

      <button class="banner__buy">
        Add to cart
      </button>
    </div>

    <div class="banner__image">
      <img
        class="image__main"
        src="images/iced-coffee.webp"
        alt="Iced Coffee"
      >

      <div class="image__users">
        <img
          v-for="(user, index) in 5"
          :key="`user-${index}`"
          :src="`images/user${index + 1}.webp`"
          alt="Users"
        >
      </div>
    </div>

    <div class="banner__features">
      <div
        v-for="(feature, index) in features"
        :key="`feature-${index}`"
        class="feature__item"
      >
        <i
          class="iconify"
          :data-icon="feature.icon"
        />
        <div class="feature__text">
          <h3>{{ feature.title }}</h3>
          <p>{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Banner',

  data() {
    return {
      features: [
        {
          title: 'Beautiful Cups',
          description: 'Cups that keep your drink tastier.',
          icon: 'raphael:coffee'
        },
        {
          title: 'Donuts',
          description: 'Enjoy our delicious and free donuts.',
          icon: 'game-icons:donut'
        },
        {
          title: 'Own coffee',
          description: 'We grow our own coffee, enjoy.',
          icon: 'fluent-mdl2:coffee'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.banner {
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 60px;
  padding-bottom: 60px;
  gap: 40px;

  @media (max-width: 839px) {
    flex-direction: column-reverse;
    text-align: center;
  }

  &__title {
    font-size: 70px;
    line-height: 70px;
    font-weight: 900;

    span {
      color: var(--primary-color);
    }
  }

  &__description {
    font-size: 18px;
    line-height: 40px;
    margin-top: 30px;
    max-width: 400px;
  }

  &__price {
    font-size: 40px;
    font-weight: 900;
    margin-top: 30px;
  }

  &__buy {
    color: #fff;
    background-color: var(--secondary-color);
    border: 1px solid var(--secondary-color);
    border-radius: var(--base-border-radius);
    padding: 20px 50px;
    font-size: 20px;
    font-weight: 600;
    margin-top: 30px;
  }

  &__image {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    width: 360px;
    height: 360px;

    &:before {
      content: "";
      background: url(images/coffe-beans.webp) bottom right/400px repeat;
      background-color: var(--secondary-color);
      width: 360px;
      height: 360px;
      position: absolute;
      border-radius: 50%;
      z-index: -1;
    }

    .image {
      &__main {
        width: 200px;
        transform: rotate(25deg);
      }

      &__users {
        position: absolute;
        display: flex;
        background-color: #fff;
        border-radius: 50px;
        padding: 10px;
        left: -140px;
        bottom: 60px;
        gap: 10px;

        @media (max-width: 991px) {
          bottom: 40px;
        }

        @media (max-width: 839px) {
          bottom: 0;
          left: inherit;
        }

        img {
          max-width: 45px;
        }
      }
    }
  }

  &__features {
    @media (max-width: 1199px) {
      display: none;
    }
    .feature {
      &__item {
        display: flex;
        align-items: center;
        max-width: 220px;

        svg {
          font-size: 100px;
          margin-right: 20px;
        }
      }

      &__text {
        h3 {
          font-weight: 900;
        }
      }
    }
  }
}
</style>