<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 1
      h1 Naturaleza de los semiconductores

    p(data-aos="fade-up") #[strong Le invitamos a observar el siguiente video, el cual precisa el concepto y la naturaleza de los semiconductores.]

    figure.mt-4
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)

    p.mt-5(data-aos="fade-up") Los elementos semiconductores se encuentran en medio de la balanza entre conductor y aislante. Cuentan usualmente con cuatro electrones de valencia y, bajo ciertas condiciones, pueden convertirse en un conductor o en un aislante; pero en su estado natural, resulta muy complejo controlar su comportamiento, por lo cual, en la producción de los componentes semiconductores que se utilizan en los equipos electrónicos, se hace necesario agregar una serie de impurezas a los materiales para lograr alterar sus propiedades y obtener un mayor control de sus propiedades conductoras o aislantes.

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 1] Comportamiento de los conductores y aislantes versus los semiconductores.

    figure.mt-5.col-md-5.m-auto
      img.image_floating(src="@/assets/curso/tema1/1.svg" data-aos="fade-up")

    figure.mt-3.col-md-9.m-auto
      img.image_floating(src="@/assets/curso/tema1/2.svg" data-aos="fade-up")

    .p-5.mt-3.caja_flotante(style="background-color:#F8F8F8")
      p(data-aos="fade-up") Los elementos semiconductores más comunes son silicio y germanio, los cuales, gracias a la adición de otros elementos, como boro, arsénico, fósforo o galio, se convierten finalmente en dispositivos semiconductores, como diodos, transistores y tiristores, a partir de los cuales se construyen todos los circuitos electrónicos. A este proceso de adición de estos elementos se le conoce comúnmente como proceso de dopaje de los semiconductores. A nivel subatómico, esto causa una variación en la cantidad de electrones de la última órbita de valencia, generando lo que se conoce como electrones libres y huecos de electrón (o simplemente huecos).

    p.mt-5(data-aos="fade-up") Después de realizar el proceso de dopaje, se obtienen como resultado dos tipos de semiconductores: tipo P y tipo N. #[strong Los tipo P] son semiconductores cuyo dopaje da como resultado un material que posee más huecos que electrones, #[strong y los tipo N] son semiconductores que poseen más electrones libres.

    .cajon.color-primario.p-5.mt-5.caja_flotante_azul
      p(data-aos="fade-up") Según Aranzabal (2001), #[strong “El átomo pentavalente en un cristal de silicio (Si) produce un electrón libre y se puede representar como un signo "+"] encerrado en un círculo y con un punto relleno (que sería el electrón) al lado.”

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 2] Semiconductor tipo N energizado

    figure.mt-4.col-md-3.m-auto
      img.image_floating(src="@/assets/curso/tema1/3.svg" data-aos="fade-up")

    .cajon.color-primario.p-5.mt-5.caja_flotante_azul
      p(data-aos="fade-up") Asimismo, de acuerdo con Aranzabal (2001): #[strong “El átomo trivalente sería un signo "-"] encerrado en un círculo y con un punto sin rellenar al lado (que simboliza un hueco).”

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 3] Semiconductor tipo P energizado

    figure.mt-4.col-md-3.m-auto
      img.image_floating(src="@/assets/curso/tema1/4.svg" data-aos="fade-up")

    figcaption.col-md-9.mt-4(data-aos="fade-up") Nota. Tomadas de Aranzabal (2001)

    p.mt-5(data-aos="fade-up") Por lo tanto, en un semiconductor dopado tipo N, los electrones aportados por la impureza superan a los huecos, mientras que en un semiconductor tipo P sucede lo contrario, los huecos superan a los electrones generados por la impureza añadida al semiconductor.

    h5.mt-5(data-aos="fade-up") A continuación se describen los tipos de semiconductores.

    .row.mt-2.col-md-11.m-auto
      .col-md-6
        p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 4] Semiconductor tipo N energizado

      .col-md-6
        p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 5] Semiconductor tipo P energizado

      .col-md-6
        .p-5.caja_flotante.caja__mostrar(style="background-color:#B3009D;border-radius:7px;height:100%;cursor:pointer;" @mouseover="eventMostrar1" v-if="!mostrar1")
          h3.text-white.text-center(data-aos="fade-up") Semiconductores tipo N

          p.mt-5.text-white(data-aos="fade-up") De acuerdo con Aranzabal (2001), en los semiconductores tipo N: “Al aplicar una tensión al semiconductor de la figura, los electrones libres dentro del semiconductor se mueven hacia la izquierda y los huecos lo hacen hacia la derecha”.

        .p-5.caja_flotante.caja__mostrar(style="background-color:#F6F6F6;border-radius:7px;height:100%;cursor:pointer;" v-if="mostrar1" @mouseleave="eventSalir1")
          h3.text-center Semiconductores tipo N
          
          br
          br
          figure.mt-5
            img.imagen_flotante_animada(src="@/assets/curso/tema1/5.svg")


      .col-md-6
        .p-5.caja_flotante.caja__mostrar(style="background-color:#3C0061;border-radius:7px;height:100%;cursor:pointer;" @mouseover="eventMostrar2" v-if="!mostrar2")
          h3.text-white.text-center(data-aos="fade-up") Semiconductores tipo P

          p.mt-5.text-white(data-aos="fade-up") Un semiconductor tipo P: “Al aplicarse una tensión, los electrones libres se mueven hacia la izquierda y los huecos lo hacen hacia la derecha. En la figura, los huecos que llegan al extremo derecho del cristal se recombinan con los electrones libres del circuito externo”. (Aranzabal, 2021)

        .p-5.caja_flotante.caja__mostrar(style="background-color:#F6F6F6;border-radius:7px;height:100%;cursor:pointer;" v-if="mostrar2" @mouseleave="eventSalir2")
          h3.text-center Semiconductores tipo P

          br
          br
          figure.mt-5
            img.imagen_flotante_animada(src="@/assets/curso/tema1/6.svg")




</template>

<script>
export default {
  name: 'Tema1',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
    mostrar1: false,
    mostrar2: false,
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
  methods: {
    eventMostrar1() {
      this.mostrar1 = true
    },
    eventMostrar2() {
      this.mostrar2 = true
    },
    eventSalir1() {
      this.mostrar1 = false
    },
    eventSalir2() {
      this.mostrar2 = false
    },
  },
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
.caja__mostrar
  transition: transform .5s linear
  -o-transition: transform .5s linear
  -ms-transition: transform .5s linear
  -moz-transition: transform .5s linear
  -webkit-transition: transform .5s linear
.caja__mostrar:hover
  transition: transform .5s linear
  -o-transition: transform .5s linear
  -ms-transition: transform .5s linear
  -moz-transition: transform .5s linear
  -webkit-transition: transform .5s linear
  transform: scale(1.04)
</style>
