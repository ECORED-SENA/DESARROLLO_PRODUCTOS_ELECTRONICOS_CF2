<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 5
      h1 #[em Software] de simulación

    p(data-aos="fade-up") Actualmente, se pueden tener a la mano una serie de herramientas que facilitan los procesos de los departamentos de ingeniería de cualquier empresa, o que son también grandes aliados de las instituciones educativas, que permiten realizar simulaciones de circuitos electrónicos simples y complejos, dando la capacidad de evaluar el comportamiento de un circuito sin necesidad de contar con él físicamente y permitiendo hacer cambios y ajustes de manera muy sencilla.

    .bloque-texto-a.color-primario.p-4.p-md-5.mt-5.caja_flotante(data-aos="fade-left")
      .row.m-0.align-items-center.justify-content-between
        .col-lg-4.mb-4.mb-lg-0
          
        .col-lg-8
          .bloque-texto-a__texto.p-5.caja_escalada_hover(style="background-color: rgb(255 255 255 / 95%);")
            p(data-aos="fade-up") En el pasado, antes de que existieran estos #[em softwares], cuando se creaba un nuevo producto, era necesario ensamblar un prototipo de prueba y cualquier cambio o modificación implicaba una cantidad considerable de tiempo y dinero, al estar cambiando constantemente de componentes.

    p.mt-5(data-aos="fade-up") Aparte de las herramientas desarrolladas por grandes empresas para el diseño electrónico, existen herramientas online que nos permiten, con algunas limitaciones, simular circuitos electrónicos de manera sencilla y gratuita; estas son una gran herramienta en el aprendizaje y puesta en práctica de cualquier aprendiz de electrónica. A continuación, se expone una de las más populares en la actualidad: EasyEDA.

    p.mt-3(data-aos="fade-up") Esta herramienta online permite simular circuitos electrónicos sencillos, así como crear proyectos para diseño de tarjetas impresas PCB. También tiene algunas características para el manejo de librerías y creación de componentes. Adicional a ello, tiene una versión descargable, también gratuita. Si se trabaja online, los proyectos son guardados en la nube del #[em software].

    .tarjeta.text-white.p-3.mt-5.caja_flotante_azul.col-md-9.m-auto(data-aos="fade-up" style="background: linear-gradient(rgb(108 0 125), rgb(226 41 255))")
      .row.justify-content-around.align-items-center
        .col-4.col-sm-2.col-lg-2
          img.p-4.imagen_flotante_animada(src="@/assets/curso/tema5/2.svg")
        .col
          .row.justify-content-between.align-items-center
            .col.mb-3.mb-sm-0
              .h2.mb-0 Tutorial de uso EasyEDA
              p.mt-3 En el recurso pdf se describe y se indica el paso a paso de cómo empezar a usarlo.
            .col-sm-auto
              a.boton.boton--b.color-acento-botones(:href="obtenerLink('downloads/tutorialEasyEDA.pdf')" target="_blank")
                span(style="color: #12263F !important;") Descargar
                i.fas.fa-file-download(style="color: #12263F !important;")



</template>

<script>
export default {
  name: 'Tema5',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
  methods: {},
}
</script>
<style lang="sass">
.image_floating
   filter: drop-shadow(10px 5px 4px rgba(0,0,0,.1))
@keyframes float
  0%
    filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
    transform: translatey(0px)
  50%
    filter: drop-shadow(26px 9px 1px rgba(0, 0, 0, 0.09))
    transform: translatey(-20px)
  100%
    filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
    transform: translatey(0px)
.imagen_flotante_animada
  filter: drop-shadow(0 5px 15px rgba(0,0,0,0.2))
  transform: translatey(0px)
  animation: float 6s ease-in-out infinite
.caja_flotante
  -webkit-box-shadow: -11px 10px 0px -1px #f3f3f3
  -moz-box-shadow: -11px 10px 0px -1px #f3f3f3
  box-shadow: -11px 10px 0px -1px #f3f3f3
.caja_escalada_hover
  transition: transform 0.5s linear
  -o-transition: transform 0.5s linear
  -ms-transition: transform 0.5s linear
  -moz-transition: transform 0.5s linear
  -webkit-transition: transform 0.5s linear
.caja_escalada_hover:hover
  transition: transform .5s ease
  transform: scale(1.06)
.fade-in-image
  animation: fadeIn 3s
  -webkit-animation: fadeIn 3s
  -moz-animation: fadeIn 3s
  -o-animation: fadeIn 3s
  -ms-animation: fadeIn 3s
@keyframes fadeIn
  0%
    opacity: 0
  100%
    opacity: 1
.tarjeta--azul
  background-color: #DBFBFF !important
.tarjeta-avatar-b > img
  min-width: 16%
  max-width: 16%
  top: -9%
.caja_flotante_azul
  box-shadow: -11px 10px 0px -1px #f1fcfd
.caja_flotante_rosada
  box-shadow: -11px 10px 0px -1px #fff6f6
.cajon.color-acento-botones
  background-color: #FFE7C4
.bloque-texto-a.color-secundario
  background-color: #F3F9FF !important
.title__tab_1 .pre
  background-color: #FFCA28
  padding: 1rem 1.5rem 1rem 1.5rem
  border-radius: 50%
  color: inherit
  font-weight: bold
  font-size: 1.3rem
  position: relative
  left: calc(100% - 147%)
  top: 2.3rem
.title__tab_1 .title
 background-color: #4DD0E1
 padding: 1rem 1rem 1rem 2rem
 border-radius: 30px
.title__tab_1
  transition: transform 0.4s linear
  -o-transition: transform 0.4s linear
  -ms-transition: transform 0.4s linear
  -moz-transition: transform 0.4s linear
  -webkit-transition: transform 0.4s linear
.title__tab_1:hover
  transition: transform .4s ease
  transform: scale(1.1)
.nav-link
  border: none !important
.nav-link.active .title__tab_1 .pre

.nav-link.active .title__tab_1 .title
  color: white
  background-color: #1565C0
.bloque-texto-a.color-primario
  background: url("../assets/curso/tema5/1.svg")
.bloque-texto-a:before
  left: 44% !important
</style>
