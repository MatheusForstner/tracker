<template>
    <footer class="rodape paragrafo">
      Desenvolvido por Matheus Forstner (Estudar Alura) | 2025 - Projeto fictício sem fins comerciais.
    </footer>
</template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent ({
    name: 'RodapeTracker'
  })
  </script>


  <style scoped>
  .rodape {
    background: #000000;
    padding: 1.5rem 7.5rem;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  @media only screen and (max-width: 1300px) {
    .rodape {
      padding: 1.5rem 3.75rem;
    }
  }
  
  @media only screen and (max-width: 767px) {
    .rodape {
      padding: 1.5rem;
    }
  }
  </style>