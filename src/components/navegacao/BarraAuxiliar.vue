<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <InfoUsuario />
  </nav>
</template>

<script>
import InfoUsuario from './InfoUsuario'
export default {
    name: 'BarraAuxiliar',
    components: {
        InfoUsuario
    }
}
</script>