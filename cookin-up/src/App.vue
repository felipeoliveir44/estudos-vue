
<script lang="ts">
// Aqui dizemos que iremos utilizar o TypeScript
// e logo fazemos a importação do componente banner do arquivo banner.vue

import Banner from './components/Banner.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';


// Para dizermos que o vue realmente precisa utilizar esse componente

export default {
  // Aqui declaramos os componentes que este componente irá usar
  // Utilizamos o export, falando que o componente que queremos usar é o banner com o valor de banner
  components: { Banner, Main, Footer }
  // Uma sintexe é quando o nome do propriedade é igual seu valor podemos deixar apenas o nome da propriedade
}
</script>

<template>
  <Banner />
  <Main></Main>
<Footer />
</template>

<style scoped>

</style>