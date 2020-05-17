<template>
    <div id="app">
        <NavegacaoGeral />
        <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>
  import NavegacaoGeral from './components/navegacao/NavegacaoGeral.vue'

  export default {
    name: 'MeuApp',
    components: {
      NavegacaoGeral
    }
  }

</script>