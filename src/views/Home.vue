<template>
  <div class="icon-bar">
    <a href="#" class="github"><i class="fa fa-github"></i></a>
    <a href="#" class="linkedin"><i class="fa fa-linkedin"></i></a>
    <a href="#" class="google"><i class="fa fa-envelope"></i></a>
    <a href="#" class="facebook"><i class="fa fa-facebook"></i></a>
  </div>
  <div class="main">
    <h1 class="app-title">UI Collections</h1>
    <div class="main__links">
      <router-link to="/gallery" class="btn--main">Gallery</router-link>
      <router-link to="/about" class="btn--main">About App</router-link>
    </div>
  </div>
  <div class="quill">
    <img :src="require(`../assets/img/feather-quill.png`)" alt="">
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.app-title {
  font-size: 10rem;
  font-family: "Arima", cursive, sans-serif;
}
.icon-bar {
  position: fixed;
  top: 50%;
  left: 0;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

.icon-bar a {
  display: block;
  text-align: center;
  padding: 16px;
  transition: all 0.3s ease;
  color: white;
  font-size: 20px;
}

.icon-bar a:hover {
  background-color: #000;
}

.facebook {
  background: #3b5998;
  color: white;
}

.github {
  background: #443c41;
  color: white;
}

.google {
  background: #dd4b39;
  color: white;
}

.linkedin {
  background: #007bb5;
  color: white;
}

.youtube {
  background: #bb0000;
  color: white;
}

.quill {
  position: fixed;
  bottom: 10rem;
  right: 10rem;
  width: 10rem;
  height: 10rem;

  img {
    width: 100%;
    height: 100%;
  }
}

.main {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__links {
    width: 100%;
    display: flex;
    justify-content: space-around;
  }
}

.btn--main {
  display: inline-block;
  border: 2px solid #000;
  border-radius: 1rem;
  font-size: 1.5rem;
  text-decoration: none;
  text-transform: uppercase;
  color: #fff;
  padding: 1.5rem 3rem;
  margin-top: 3rem;
  background-color: #1a2934;
  cursor: pointer;
  z-index: 10000;
}
</style>