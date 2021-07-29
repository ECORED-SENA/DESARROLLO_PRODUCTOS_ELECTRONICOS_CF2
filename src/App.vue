<template lang="pug">
#app.app
  Header
  .contenedor-principal
    AsideMenu
    section.seccion-principal(:class="{'seccion-principal--barra-avance-open' : !menuState}")
      router-view
  BarraAvance
  Accesibilidad
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    menuOpen: false,
  }),
  computed: {
    menuState() {
      return this.$store.getters.isMenuOpen
    },
  },
  mounted() {
    this.$aos.init({
      offset: 100,
    })
  },
}
</script>
<style lang="sass">
.curso-main-container > .container
  overflow-x: unset !important
.titulo-principal__numero
  background-color: #b3009d !important
.titulo-principal__numero span
  color: #ffffff !important
@keyframes float
  0%
    filter: drop-shadow(3px 0px 3px yellow)
    transform: translatey(0px)
  50%
    filter: drop-shadow(3px 0px 6px yellow)
    transform: translatey(-20px)
  75%
    filter: drop-shadow(3px 0px 10px yellow)
    transform: translatey(-20px)
  100%
    filter: drop-shadow(3px 0px 2px yellow)
    transform: translatey(0px)
.banner-principal__img img
  filter: drop-shadow(0px 0px 1px yellow)
  transform: translatey(0px)
  animation: float 7s ease-in-out infinite
.cajon.color-primario
  background-color: #CBFFF6 !important
</style>
