<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <a class="navbar-brand" href="#">Loopa</a>

      <button v-on:click.prevent="mensagem()"
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div v-if="!mobile" class="collapse navbar-collapse" id="navbarSupportedContent">
        <ItensSuperiores/>
      </div>

      <InfoUsuario v-if="!mobile" />

      <Avatar style="border: 1px solid green; float: right;" />
    </nav>

    <div v-if="mobile">
      <BarraAuxiliar />
    </div>
  </div>
</template>

<script>
import Avatar from "./Avatar";
import ItensSuperiores from "./ItensSuperiores";
import InfoUsuario from "./InfoUsuario";
import BarraAuxiliar from "./BarraAuxiliar";
export default {
  name: "NavBarSuperior",
  components: {
    Avatar,
    ItensSuperiores,
    InfoUsuario,
    BarraAuxiliar
  },

  created: function() {
    window.addEventListener("resize", () => {
      this.size = window.innerWidth;
    });
  },

  data: () => {
    return {
      size: window.innerWidth
    };
  },

  computed: {
    mobile: function() {
      return this.size < 1000;
    }
  },

  methods: {
    mensagem: () => {
      alert("implementar sidebar...")
    }
  }
};
</script>