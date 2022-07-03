<template>
  <div :style="{backgroundColor: props.colour}" class="container">
    <slot></slot>
  </div>
</template>

<script setup>
const props = defineProps({
  colour: String,
});
</script>

<style lang="scss" scoped>
.container {
  width: 100vw;
  height: 100vh;
  display: grid;
  place-items: center;
}
</style>