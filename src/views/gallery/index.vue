<template>
  <button @click="previousSlide" class="btn btn--left">&lsaquo;</button>
  <input @keyup.left="previousSlide" type="hidden" name="left">

  <Container :colour="currentBgColour">
    <component :is="currentComponent"></component>
  </Container>

  <button @click="nextSlide" class="btn btn--right">&rsaquo;</button>
</template>

<script setup>
import { ref, reactive, computed, watch } from "vue";
import Container from "../../components/Container.vue";
import EauDeParfum from "../../components/components/EauDeParfum.vue";
import BaseApparel from "../../components/components/BaseApparel.vue";
import NFT from "../../components/components/NFT.vue";
import QRCode from "../../components/components/QRCode.vue";
const index = ref(0);
const state = reactive({
  components: [BaseApparel, EauDeParfum, NFT, QRCode], //NOTEIMPORTANT: values in this array (the components) should NOT be strings; not "". it won't work
  backgroundColours: ["rgb(231, 157, 157)", "rgb(242, 235, 227)", "rgb(13, 25, 43)", "rgb(214, 226, 240)"],
});

const currentComponent = computed(() => state.components[index.value]);
const currentBgColour = computed(() => state.backgroundColours[index.value]);

function nextSlide() {
  index.value += 1;
  if (index.value > state.components.length - 1) index.value = 0;
}

function previousSlide() {
  index.value -= 1;
  if (index.value < 0) index.value = state.components.length - 1;
}

watch(currentComponent, () => {
  console.log(currentComponent.value);
});
</script>

<style lang="scss" scoped>
.btn {
  all: unset; /* que j'aime ce feature */
  font-size: 8.5rem;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  cursor: pointer;

  &--left {
    left: 2rem;
  }

  &--right {
    right: 2rem;
  }
}
</style>
