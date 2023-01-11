<template>
  <img v-if="!isBg" :src="src" :alt="alt" :class="$style['img-image']">
  <div v-else :style="{backgroundImage: src}" :class="$style['bg-image']" />
</template>

<script>
export default {
  name: 'VImage',
  props: {
    fileName: String,
    alt: {
      type: String,
      default: '',
    },
    isBg: {
      type: Boolean,
      default: false,
    }
  },
  computed: {
    src() {
      const src = require('../assets/images/' + this.fileName);
      return this.isBg ? 'url(' + src + ')' : src;
    }
  },
}
</script>

<style lang="scss" module>
.img-image {
  //width: 100%;
}
.bg-image {
  background: center/cover no-repeat;
}
</style>
