<template>
  <div class="ui-container">
    <div class="card__image">
      <img :src="require(`../../assets/img/nft/image-equilibrium.jpg`)" alt="">
    </div>
    <div class="card__content">
      <h2>Equilibrium #7264</h2>
      <p>Our Equilibrium collection promotes balance and calm.</p>
      <div>
        <p>
          <img :src="require(`../../assets/img/nft/icon-ethereum.svg`)" alt="">
          <span>0.041ETH</span>

        </p>
        <p>
          <img :src="require(`../../assets/img/nft/icon-clock.svg`)" alt="">
          <span>3 days left</span>
        </p>
      </div>
    </div>
    <div class="card__credentials">
      <img :src="require(`../../assets/img/nft/image-avatar.png`)" alt="">
      <span>Creation of <span>Jules Wyvern</span></span>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.ui-container {
  width: 35rem;
  height: 60vh;
  background-color: rgb(20, 37, 61);
  border-radius: 2rem;
  display: grid;
  grid-template-rows: 32.5rem repeat(2, 1fr);
}

.card {
  &__image {
    width: 100%;
    padding: 2rem;

    img {
      width: 100%;
      height: 100%;
      border-radius: 1.25rem;
    }
  }
}
</style>