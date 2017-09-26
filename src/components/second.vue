<template>
  <transition name="slide-right">
    <div class="test">
      <h2>second</h2>
      <button @click="prev"> ◀ </button>
    </div>
  </transition>
</template>

<script>
  export default {
    methods: {
      prev: function () {
        this.$router.push({name: 'first'});
      }
    }
  }
</script>

<style>
  /** transitionのアニメーション **/
  .slide-right-enter-active, .slide-right-leave-active {
    position: absolute;
    margin-left: 0;
    -webkit-transition: opacity .5s, margin-left .5s linear;
  }
  .slide-right-enter, .slide-right-leave-to {
    opacity: 0;
    position: absolute;
    margin-left: 100px;
  }
</style>
