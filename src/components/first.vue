<template>
  <div>
    <h2>first</h2>
    <button @click="next"> ▶ </button>
  </div>
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
