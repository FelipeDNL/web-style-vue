<script setup lang="ts">
</script>

<template>
  <div class="content">

    <div class="main-page">
      <h1>フィリップ</h1>
    </div>

    <div class="letters">
      <div class="scrolling-letters-1">
        <p>日本語の話し方がわかりません</p>
      </div>

      <div class="scrolling-letters-2">
        <p>Meu app vue.js</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.content {
  display: flex;
  height: 98vh;
  overflow: hidden;
  white-space: nowrap;
}

.main-page {
  flex: 1;
}

.scrolling-letters-1 {
  writing-mode: vertical-rl;
  font-size: 60px;
  color: brown;
  padding-right: 40px;

  /* animation properties */
  -moz-transform: translateY(-100%);
  -webkit-transform: translateY(-100%);
  transform: translateY(-100%);

  -moz-animation: my-animation-2 3s linear infinite;
  -webkit-animation: my-animation-2 3s linear infinite;
  animation: my-animation-2 3s linear infinite;
}

.scrolling-letters-2 {
  writing-mode: sideways-rl;
  font-size: 120px;
  color: brown;

  /* animation properties */
  -moz-transform: translateY(100%);
  -webkit-transform: translateY(100%);
  transform: translateY(100%);

  -moz-animation: my-animation-1 15s linear infinite;
  -webkit-animation: my-animation-1 15s linear infinite;
  animation: my-animation-1 15s linear infinite;
}

/* for Chrome */
@-webkit-keyframes my-animation-1 {
  from {
    -webkit-transform: translateY(100%);
  }

  to {
    -webkit-transform: translateY(-100%);
  }
}

@keyframes my-animation-1 {
  from {
    -moz-transform: translateY(100%);
    -webkit-transform: translateY(100%);
    transform: translateY(100%);
  }

  to {
    -moz-transform: translateY(-100%);
    -webkit-transform: translateY(-100%);
    transform: translateY(-100%);
  }
}

/* for Chrome */
@-webkit-keyframes my-animation-2 {
  from {
    -webkit-transform: translateY(-100%);
  }

  to {
    -webkit-transform: translateY(100%);
  }
}

@keyframes my-animation-2 {
  from {
    -moz-transform: translateY(-100%);
    -webkit-transform: translateY(-100%);
    transform: translateY(-100%);
  }

  to {
    -moz-transform: translateY(100%);
    -webkit-transform: translateY(100%);
    transform: translateY(100%);
  }
}
</style>
