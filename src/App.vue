<script setup lang="ts">
</script>

<template>
  <div class="content">
    <div class="main-page">
      <h1>日本語の話し方がわかりません</h1>
    </div>

    <div class="letters">
      <div class="scrolling-letters-1">
        <p>フィリップ</p>
      </div>

      <div class="scrolling-letters-2">
        <p class="p-big">Life's getting quite exciting</p>
      </div>

    </div>
  </div>
</template>

<style scoped>
.content {
  display: flex;
  height: 98vh;
  overflow: hidden; /* Impede a barra de rolagem */
  
}

.main-page {
  flex:1;
  display: flex;
}

.letters {
  white-space: nowrap; /* Impede a quebra de linha */
}

.p-big {
  margin-right: 60px
}

.scrolling-letters-1 {
  writing-mode: vertical-rl;
  font-size: 60px;
  color: brown;

  /* animation properties */
  transform: translateY(100%);

  animation: animacao-cima-baixo 4s linear infinite; /* Aplica a animação `animacao-baixo-cima` no padrão, com duração de 10s, linear e infinita. */
}

.scrolling-letters-2 {
  writing-mode: sideways-rl; /* Define o texto para ser escrito na direção horizontal, mas rotacionado para a direita. */
  font-size: 120px; /* Define o tamanho da fonte como 120px. */
  color: brown; /* Define a cor do texto como marrom. */
  /* Propriedades de transformação inicial */
  transform: translateY(-100%); /* Move o elemento 100% para baixo no eixo Y (padrão). */

  /* Propriedades de animação */
   animation: animacao-baixo-cima 10s linear infinite; /* Aplica a animação `animacao-cima-baixo` no padrão, com duração de 10s, linear e infinita. */
}

@keyframes animacao-baixo-cima {
  from {
    transform: translateY(35%); /* Início da animação no padrão: o elemento está 100% abaixo do eixo Y. */
  }

  to {
    transform: translateY(-115%); /* Fim da animação no padrão: o elemento está 100% acima do eixo Y. */
  }
}

@keyframes animacao-cima-baixo {
  from {
    transform: translateY(-120%);
  }

  to {
    transform: translateY(320%);
  }
}

@media (max-width: 768px) {
  .p-big {
    margin-right: 0px;
  }
  
}
</style>
