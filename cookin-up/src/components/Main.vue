<script lang="ts">
import SelecionarIngredientes from './SelecionarIngredientes.vue';
import SuaLista from './SuaLista.vue';

export default {
  data() {
    return {
      ingredientes: [] as string[]
    };
  },
  components: { SelecionarIngredientes, SuaLista },
  methods: {
    adicionarIngrediente(ingrediente: string) {
      this.ingredientes.push(ingrediente)
    },
    removerIngrediente(ingrediente: string) {
  this.ingredientes = this.ingredientes.filter(iLista => ingrediente !== iLista);
},
  }
}
</script>

<template>
  <main class="conteudo-principal">
    <SuaLista :ingredientes="ingredientes" />
    <SelecionarIngredientes
  @adicionar-ingrediente="adicionarIngrediente"
  @remover-ingrediente="removerIngrediente"
/>
  </main>
</template>

<style>
.conteudo-principal {
  padding: 6.5rem 7.5rem;
  border-radius: 3.75rem 3.75rem 0rem 0rem;
  background: var(--creme, #FFFAF3);
  color: var(--cinza, #444);

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5rem;
}
</style>