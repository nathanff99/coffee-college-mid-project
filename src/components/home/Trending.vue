<template>
  <section id="trending" class="trending">
    <div class="trending__list coffee-container">
      <article
        v-for="(item, index) in 4"
        :key="`trending-${index}`"
        class="trending__item"
      >
        <img
          class="item__image"
          src="images/iced-coffee.webp"
          alt="Iced Coffee"
        />

        <h3 class="item__title">Iced Coffe</h3>
        <a class="item__action">Add to cart +</a>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  name: "trending",
};
</script>

<style lang="scss" scoped>
.trending {
  background: var(--secondary-color);

  &__list {
    display: flex;
    justify-content: center;
    gap: 60px;
    height: 100%;
    flex-wrap: wrap;
    margin-top: -320px;
    padding-bottom: 60px;
  }

  &__item {
    display: flex;
    flex-direction: column;
    color: #fff;
    align-items: center;
    z-index: 1;
    padding: 40px 40px 0;
    gap: 10px;
  }

  .item {
    &__image {
      max-width: 150px;
    }

    &__title {
      font-size: 30px;
      font-weight: 900;
    }

    &__action {
      cursor: pointer;
    }
  }
}
</style>