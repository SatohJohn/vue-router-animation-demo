<template>
  <div>
    <h2>second</h2>
    <button @click="prev"> ◀ </button>
  </div>
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
