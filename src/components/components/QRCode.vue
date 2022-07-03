<template>
  <div class="ui-container">
    <div class="card__image">
      <img :src="require(`../../assets/img/qr-code/image-qr-code.png`)" alt="">
    </div>
    <h2 class="card__title">Improve your front-end skills by building projects</h2>
    <p class="card__paragraph">
      Scan the QR code to visit Frontend Mentor and take your coding skills to the next level
    </p>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.ui-container {
  width: 35rem;
  //   height: 60vh;
  background-color: #fff;
  border-radius: 2rem;
  display: grid;
  grid-template-rows: 32.5rem repeat(2, min-content);

  & > *:not(.card__image) {
    margin: 2rem 0;
    padding: 0 3rem;
    text-align: center;
  }
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

  &__title {
    font-size: 2.25rem;
    color: rgb(31, 50, 81);
  }

  &__paragraph {
    font-size: 1.5rem;
    padding-bottom: 2.5rem !important;
    color: rgb(123, 135, 157);
  }
}
</style>