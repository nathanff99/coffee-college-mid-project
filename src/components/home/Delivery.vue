<template>
  <section
    id="delivery"
    class="delivery"
  >
    <div class="coffee-container">
      <div class="delivery__text">
        <h2>We are in the best apps</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>

      <div class="delivery__list">
        <img
          v-for="(app, index) in apps"
          :key="`app-${index}`"
          class="delivery__item"
          :src="`images/${app.image}`"
          :alt="app.name"
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Delivery',

  data() {
    return {
      apps: [
        { name: 'Doordash', image: 'doordash.webp' },
        { name: 'Uber Eats', image: 'uber-eats.webp' },
        { name: 'Skip The Dishes', image: 'skip-the-dishes.webp' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.delivery {
  display: flex;
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--secondary-color);

  &__text {
    color: #fff;
    text-align: center;
    max-width: 700px;

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

  &__list {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    margin-top: 40px;
    gap: 40px;
  }

  &__item {
    max-width: 180px;
  }
}
</style>