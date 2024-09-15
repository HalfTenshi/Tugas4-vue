<template>
  <div id="app">
    <ImageCarousel />
    <BoxColorChanger />
    <ClickCounter />
  </div>
</template>

<script>
import BoxColorChanger from './components/BoxColorChanger.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import ClickCounter from './components/ClickCounter.vue';

export default {
  components: {
    ImageCarousel,
    BoxColorChanger,
    ClickCounter,
  },
};
</script>