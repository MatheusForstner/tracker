<template>
    <header>
            <h1 class="irish">Tracker</h1>
            <button class="modo" @click="alterarTema" >
              <i class="fa-solid fa-circle-half-stroke"></i>
                {{ textoBotao }}
            </button>
    </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'BarraLateral',
    emits: ['aoTemaAlterado'],
    data () {
    return {
      modoEscuroAtivo: false
    }
  },
  computed: {
    textoBotao () {
      if (this.modoEscuroAtivo) {
        return 'Modo Claro'
      }
      return 'Modo Escuro'
    }
  },
  methods: {
    alterarTema () {
      this.modoEscuroAtivo = !this.modoEscuroAtivo
      this.$emit('aoTemaAlterado', this.modoEscuroAtivo)
    }
  }
})
</script>

<style scoped>
/* todo o estilo do componente */

    header {
    padding: 1rem;
    background-image: linear-gradient(to right bottom, 
     rgba(10, 10, 10, 0.808),
     rgba(43, 43, 43, 0.8)), 
    url('https://i.pinimg.com/originals/10/f9/33/10f9334410a5c59d0e8d1a5258ed8ba2.jpg');
    width: 90%;
    height: 900px;
    background-size: cover;


    }
    .modo{
      left: 90px;
      display: flex;
    }

    .modo i {
      padding: 4px;
    }


/* CSS */
.modo {
  align-items: center;
  background-color: #FFFFFF;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: .25rem;
  box-shadow: rgba(0, 0, 0, 0.02) 0 1px 3px 0;
  box-sizing: border-box;
  color: rgba(0, 0, 0, 0.85);
  cursor: pointer;
  display: inline-flex;
  font-family: system-ui,-apple-system,system-ui,"Helvetica Neue",Helvetica,Arial,sans-serif;
  font-size: 16px;
  font-weight: 600;
  justify-content: center;
  line-height: 1.25;
  margin: 0;
  min-height: 3rem;
  padding: calc(.875rem - 1px) calc(1.5rem - 1px);
  position: relative;
  text-decoration: none;
  transition: all 250ms;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  vertical-align: baseline;
  width: auto;
}

.modo:hover,
.modo:focus {
  border-color: rgba(0, 0, 0, 0.15);
  box-shadow: rgba(0, 0, 0, 0.1) 0 4px 12px;
  color: rgba(0, 0, 0, 0.65);
}

.modo:hover {
  transform: translateY(-1px);
}

.modo:active {
  background-color: #F0F0F1;
  border-color: rgba(0, 0, 0, 0.15);
  box-shadow: rgba(0, 0, 0, 0.06) 0 2px 4px;
  color: rgba(0, 0, 0, 0.65);
  transform: translateY(0);
}

    .irish {
        font-family: "Poppins", sans-serif;
        font-weight: 800;
        color: #eee;
        font-size: 3em; 
        text-align: center;
    }
    @media only screen and (max-width: 768px) {
    header {
        padding: 2.5rem;
        height: auto;
    }
    }
</style>