<template>
  <div class="text-loading">
    <span v-for="(item, i) in text" :key="i" class="text-loading__span">{{
      item
    }}</span>
  </div>
</template>

<script>
export default {
  name: '',
  props: {
    loadingText: {
      type: String,
      default: 'Fsleep'
    }
  },
  data() {
    return {}
  },
  computed: {
    text() {
      return this.loadingText.split('')
    }
  },
  watch: {},
  methods: {}
}
</script>

<style lang="scss" scoped>
.text-loading {
  position: fixed;
  z-index: 99999;
  opacity: 0.4;
  height: 100vh;
  width: 100vw;
  background: var(--black);
  overflow: hidden;
  font: 5vw / 100vh 'Finger Paint';
  text-align: center;
  color: transparent;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  top: 0;
  left: 0;

  &__span {
    display: inline-block;
    text-shadow: 0 0 0 var(--white);
    animation: smoky 2s 2s both;

    &:nth-child(even) {
      animation-name: smoky-mirror;
    }

    &:nth-of-type(1) {
      animation-delay: 1s;
    }

    &:nth-of-type(2) {
      animation-delay: 1.1s;
    }

    &:nth-of-type(3) {
      animation-delay: 1.2s;
    }

    &:nth-of-type(4) {
      animation-delay: 1.3s;
    }

    &:nth-of-type(5) {
      animation-delay: 1.4s;
    }

    &:nth-of-type(6) {
      animation-delay: 1.5s;
    }

    &:nth-of-type(7) {
      animation-delay: 1.6s;
    }

    &:nth-of-type(8) {
      animation-delay: 1.7s;
    }

    &:nth-of-type(9) {
      animation-delay: 1.8s;
    }

    &:nth-of-type(10) {
      animation-delay: 1.9s;
    }

    &:nth-of-type(11) {
      animation-delay: 2s;
    }

    &:nth-of-type(12) {
      animation-delay: 2.1s;
    }
  }
}

@keyframes smoky {
  60% {
    text-shadow: 0 0 40px var(--white);
  }

  to {
    transform: translate3d(15rem, -8rem, 0) rotate(-40deg) skewX(70deg) scale(1.5);
    text-shadow: 0 0 20px var(--white);
    opacity: 0;
  }
}

@keyframes smoky-mirror {
  60% {
    text-shadow: 0 0 40px var(--white);
  }

  to {
    transform: translate3d(18rem, -8rem, 0) rotate(-40deg) skewX(-70deg) scale(2);
    text-shadow: 0 0 20px var(--white);
    opacity: 0;
  }
}
</style>
