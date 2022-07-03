<template>
  <div class="ui-container">
    <div class="left">
      <!-- <img :src="require(`../../assets/img/logo.svg`)" class="logo"> -->
      <div class="left__content">
        <img :src="require(`../../assets/img/base-apparel/logo.svg`)" class="logo">
        <h1 class="header-title">
          <span class="header-title__light">We're </span>
          <span class="header-title__dark">Coming</span>
          <span class="header-title__dark">Soon</span>
        </h1>

        <p class="paragraph">
          Hello fellow shoppers! We're currently building our new fashion store.
          Add your email below to stay up-to-date with announcements and our launch deals.
        </p>

        <form id="form">
          <!-- NOTE: Changer le type d'input de e-mail à text pour que tout puisse bien marcher -->
          <input type="text" id="email" class="email" placeholder="E-mail Address">
          <button type="submit" class="btn">
            <img src="../../assets/img/base-apparel/icon-arrow.svg" alt="iconarrow">
          </button>
        </form>
        <span id="form-status" class="form-status"></span>

      </div>

    </div>
    <div class="right"></div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
$text-colour: #ffccd5;
.ui-container {
  position: relative;
  width: 110rem;
  // height: 60vh;
  display: grid;
  grid-template-columns: 55% 1fr;
  -webkit-box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.4);
  box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.4);

  .left {
    // removing (but keeping code for now) the dynamic bgColour gets in the way of the form. z-index ne le resourde pas
    // background-image: url(~@/assets/img/base-apparel/bg-pattern-desktop.svg);
    // background-size: cover;
    // background-color: #f5d9cd;
    background-color: #fceae3;
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
      height: 65rem;
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      -webkit-box-orient: vertical;
      -webkit-box-direction: normal;
      -ms-flex-direction: column;
      flex-direction: column;
      -webkit-box-pack: justify;
      -ms-flex-pack: justify;
      justify-content: space-between;
      -webkit-box-align: start;
      -ms-flex-align: start;
      align-items: flex-start;
      padding: 3rem 0;
    }
  }

  .right {
    background-image: url(~@/assets/img/base-apparel/hero-desktop.jpg);
    background-size: cover;
  }
}

.logo {
  // NOTE:NEW: although in flex container, position: absolute, takes it out of flex flow. C'est très cool et très idéal
  //   position: absolute;
  //   top: 1rem;
  //   left: 1rem;
}

.header-title {
  & > * {
    display: block;
    letter-spacing: 10px;
    text-transform: uppercase;
  }

  &__light {
    font-weight: 300;
    color: rgb(206, 151, 151);
    font-size: 5rem;
  }

  &__dark {
    font-size: 4.5rem;
    font-weight: 500;
  }
}

.paragraph {
  color: rgb(231, 157, 157);
  font-size: 1.6rem;
  line-height: 1.25;
}

form {
  position: relative;
  width: 100%;
}

.btn {
  position: absolute;
  top: 0;
  right: 11.25rem;
  color: #fff;
  font-size: 2.5rem;
  outline: none;
  border: none;
  border-radius: 3rem;
  padding: 1.5rem 3.5rem;
  background-image: -webkit-gradient(linear, left top, right top, from(hsl(0, 93%, 68%)), to(hsl(0, 36%, 70%)));
  background-image: linear-gradient(to right, hsl(0, 93%, 68%), hsl(0, 36%, 70%));
  cursor: pointer;
}

.email {
  border: 1.5px solid rgb(230, 223, 223);
  border-radius: 4rem;
  outline: none;
  padding: 2rem 2rem;
  width: 75%;
  font-family: inherit;
  font-size: 1.5rem;
}

.form-status {
  font-size: 1.5rem;

  &.valid {
    color: rgb(250, 104, 104);
  }

  &.invalid {
    color: rgb(156, 33, 33);
  }
}
</style>