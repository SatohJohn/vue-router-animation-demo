<template>
  <transition name="slide-left">
    <div class="test">
      <h2>first</h2>
      <button @click="next"> ▶ </button>
    </div>
  </transition>
</template>

<script>
  export default {
    methods: {
      next: function () {
        this.$router.push({name: 'second'});
      }
    }
  }
</script>

<style>
  /** transitionのアニメーション **/
  .slide-left-enter-active, .slide-left-leave-active {
    position: absolute;
    margin-left: 0;
    -webkit-transition: opacity .5s, margin-left .5s linear;
  }
  .slide-left-enter, .slide-left-leave-to {
    opacity: 0;
    position: absolute;
    margin-left: -100px;
  }
</style>
