<template>
  <section
    id="about"
    class="about"
  >
    <ShapeOne class="about__shape" />

    <div class="about__content coffee-container">
      <img
        class="about__image"
        src="images/iced-coffee-hand.webp"
        alt="Iced Coffee"
      >

      <div class="about__text">
        <h2>The best coffee in your home town</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur.
        </p>
      </div>
    </div>

    <ShapeTwo class="about__shape-two" />
  </section>
</template>

<script>
import ShapeOne from '../shapes/ShapeOne.vue'
import ShapeTwo from '../shapes/ShapeTwo.vue'

export default {
  name: 'About',

  components: {
    ShapeOne,
    ShapeTwo
  }
}
</script>

<style lang="scss" scoped>
.about {
  position: relative;
  background: #fff;
  padding-top: 300px;
  padding-bottom: 400px;

  &__shape {
    position: absolute;
    top: 0;
    right: 0;
  }

  &__shape-two {
    position: absolute;
    bottom: 0;
    right: 0;
  }

  &__content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 60px;

    @media (max-width: 991px) {
      flex-direction: column;
      text-align: center;
    }
  }

  &__image {
    max-width: 100%;
  }

  &__text {
    h2 {
      font-weight: 900;
      font-size: 40px;
      text-transform: uppercase;
      margin-bottom: 30px;
    }

    p {
      font-size: 18px;
      line-height: 30px;
    }
  }
}
</style>