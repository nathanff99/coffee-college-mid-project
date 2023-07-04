<template>
  <section
    id="contact"
    class="contact"
  >
    <div class="coffee-container">
      <div class="contact__text">
        <h2>Contact Us</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </p>
      </div>

      <form class="contact__form">
        <input
          type="text"
          class="contact__input"
          placeholder="Name"
        >
        <input
          type="email"
          class="contact__input"
          placeholder="E-mail"
        >
        <textarea
          name="message"
          class="contact__input"
          placeholder="Message"
        />
        <button
          class="contact__button"
          type="submit"
        >
          Send
        </button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact'
}
</script>

<style lang="scss" scoped>
.contact {
  display: flex;
  justify-content: center;
  background-color: var(--secondary-color);
  padding-bottom: 60px;

  &__text {
    color: #fff;
    text-align: center;
    max-width: 600px;
    margin-bottom: 40px;

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

  &__form {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 20px;
  }

  &__input {
    padding: 10px;
    background-color: #574045;
    border: 1px solid #574045;
    outline: none;
    color: #fff;
    font-size: 18px;
    border-radius: 10px;
    height: 60px;
    width: 100%;
    max-width: 600px;
  }

  &__button {
    padding: 10px;
    background-color: #35282b;
    border: 1px solid #35282b;
    color: #fff;
    font-size: 18px;
    font-weight: 900;
    border-radius: 10px;
    height: 60px;
    width: 100%;
    max-width: 600px;
    cursor: pointer;
  }

  textarea {
    min-height: 100px;
  }

  ::-webkit-input-placeholder {
    color: #fff;
  }
  :-moz-placeholder {
    color: #fff;
    opacity: 1;
  }
  ::-moz-placeholder {
    color: #fff;
    opacity: 1;
  }
  :-ms-input-placeholder {
    color: #fff;
  }
  ::-ms-input-placeholder {
    color: #fff;
  }

  ::placeholder {
    color: #fff;
  }
}
</style>