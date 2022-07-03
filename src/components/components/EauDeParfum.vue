<template>
  <div class="ui-container">

    <div class="left"></div>
    <div class="right">
      <div class="right__content">
        <h5>Perfume</h5>
        <h1 class="header__title">
          <span class="header-title__light">Gabrielle</span>
          <span class="header-title__dark">Essence Eau De</span>
          <span class="header-title__dark">Parfum</span>
        </h1>

        <p class="paragraph">
          A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL
        </p>

        <p class="prices">
          <span class="prices__sale">$149.99</span>
          <span class="prices__original">$169.99</span>
        </p>

        <button type="submit" class="btn">
          <span>Add to Cart</span>
          <img src="../../assets/img/eau-de-parfum/icon-cart.svg" alt="iconcart">
        </button>
      </div>

    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.ui-container {
  position: relative;
  width: 80rem;
  // height: 50vh;
  // height: auto;
  display: grid;
  grid-template-columns: 55% 1fr;
  -webkit-box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.4);
  box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.4);

  .left {
    background-image: url(~@/assets/img/eau-de-parfum/image-product-desktop.jpg);
    background-size: cover;
    background-position: center;
  }
  .right {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;

    &__content {
      width: 80%;
      height: 50rem;
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      // -webkit-box-orient: vertical;
      // -webkit-box-direction: normal;
      // -ms-flex-direction: column;
      // flex-direction: column;
      // -webkit-box-pack: justify;
      // -ms-flex-pack: justify;
      // justify-content: space-between;
      // -webkit-box-align: start;
      // -ms-flex-align: start;
      // align-items: flex-start;
      flex-direction: column;
      justify-content: space-around;
      // padding: 3rem 0;
    }
  }
}

.header__title {
  font-family: "Fraunces", serif;
  font-size: 4rem;
  color: rgb(28, 35, 43);

  span {
    display: block;
  }
}

.paragraph {
  font-size: 1.4rem;
  font-size: "Montserrat", sans-serif;
  color: rgb(108, 114, 137);
}

.prices {
  display: flex;
  align-items: center;

  &__sale {
    font-size: 4rem;
    font-family: "Fraunces", serif;

    color: hsl(158, 36%, 37%);
    margin-right: 2.5rem;
  }

  &__original {
    font-size: 1.5rem;
    color: hsl(228, 12%, 48%);
    text-decoration: line-through;
  }
}
</style>