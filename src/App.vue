<script setup lang="ts">
</script>

<template>
  <div id="app">

    <div class="content">
      <h1>Welcome to Your Vue.js App</h1>
    
    <div class="scrolling-letters">
      <p>This is a simple Vue.js application.</p>
    </div>

  </div>
  </div>
</template>

<style scoped>

  .content {
    display: flex;
  }

  .scrolling-letters {
    flex: 1;
    writing-mode: sideways-rl;
    white-space: nowrap;
    font-size: 120px;
    color: rgb(199, 12, 12);
  }

</style>
