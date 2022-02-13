<template>
  <button @click="changeFlag">Toggle</button>

  <transition name="fade">
    <h2 v-if="flag">Hello, World</h2>
  </transition>
</template>

<script>

export default {
  name: 'App',
  methods: {
    changeFlag() {
      this.flag = !this.flag;
    }
  },
  data() {
    return {
      flag: false,
    }
  }
};
</script>

<style>
.fade-enter-from {
  opacity: 0;
}

.fade-enter-active {
  transition: all 0.25s linear;
}

.fade-leave-to {
  transition: all 0.25s linear;
  opacity: 0;
}
</style>
