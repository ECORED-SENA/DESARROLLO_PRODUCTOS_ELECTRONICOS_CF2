<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 4
      h1 Tiristores

    p(data-aos="fade-up") Los tiristores, en términos generales, son semiconductores de potencia, que al igual que los demás dispositivos semiconductores, gracias a diferentes configuraciones en el circuito, pueden controlar su forma de conducción para ser aislantes o conductores en ciertos momentos. Revise, a continuación, los tipos de tiristores.

    .row.mt-5
      .col-md-3.indicador__container
        .p-5.caja_flotante.caja_escalada_hover.caja__activa1.caja__1.mb-4(style="background-color:#B3009D;border-radius:10px;cursor:pointer;" @click="eventoMostrar1")
          h3.text-center.text-white(data-aos="fade-up") Tiristor SCR
          .indicador--click(v-if="mostrarIndicador")

        .p-5.mt-3.caja_flotante.caja_escalada_hover.caja__2(style="background-color:#00CCA7;border-radius:10px;cursor:pointer;" @click="eventoMostrar2")
          h3.text-center.text-white(data-aos="fade-up") Tiristor TRIAC

      .col-md-9
        div(v-if="mostrar1")
          .p-5(style="background-color:#F3F9FF;border-radius:8px;" data-aos="fade-right")
            h4(data-aos="fade-up") Rectificador controlado de silicio SCR

            p.mt-4(data-aos="fade-up") El tiristor más simple es el SCR (que viene de su nombre en inglés, #[em Silicon Controlled Rectifier]). Básicamente, es un diodo que cuenta con un tercer pin de compuerta que le sirve para hacer un control primario de su conducción; este pin se conoce como compuerta (#[em gate]).

            p.mt-3(data-aos="fade-up") Un SCR, como cualquier rectificador, requiere estar correctamente polarizado y superar el voltaje umbral, además de recibir un pequeño pulso de corriente y un mínimo voltaje a través de su compuerta. Estos datos usualmente los brinda el fabricante del dispositivo, pero a diferencia de los transistores, por ejemplo, él no requiere mantener esa corriente, es un disparo momentáneo que lo activa y, mientras sus demás condiciones de polarización entre ánodo y cátodo se mantengan, este se mantendrá conduciendo.

            p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 23] Aspecto físico y simbología del SCR

            .bg-white.p-3.row.mt-4(style="border: 1px #707070 solid")
              .col-md-5.text-center.mb-3
                h4(data-aos="fade-up") Tiristor Real

                figure.mt-3
                  img(data-aos="fade-up" src="@/assets/curso/tema4/1.svg")

              .col-md-2

              .col-md-5.text-center.mb-3
                h4(data-aos="fade-up") Símbolo del tiristor

                figure.mt-3
                  img(data-aos="fade-up" src="@/assets/curso/tema4/2.svg")

            figcaption.col-md-9.mt-3(data-aos="fade-up") Nota. Tomada de Ingeniería Mecafenix (2018).

            h4.mt-5(data-aos="fade-up") Rectificador controlado de silicio SCR

            h5.mt-4(data-aos="fade-up") Control del ángulo de disparo del SCR

            p.mt-4(data-aos="fade-up") El uso del SCR en corriente directa no es muy práctico, ya que sería un dispositivo que se dispararía a conducir y por la naturaleza de la corriente DC estaría en ese estado todo el tiempo, activado y conduciendo corriente. El uso más amplio de estos dispositivos electrónicos de potencia es con el aprovechamiento y control de potencia de cargas en corriente alterna o AC.

            p.mt-3(data-aos="fade-up") Dada la forma de onda de la corriente AC, un SCR solo podría conducir corriente en el semiciclo positivo de la onda AC, ya que en el semiciclo negativo este estaría polarizado inversamente. Si se activa la compuerta del SCR con un disparo de corriente y voltaje adecuados, conducirá solo si está en el semiciclo positivo. Cuando viene el semiciclo negativo, este deja de conducir y se inactiva y volverá a conducir cuando se vuelva a enviar el impulso y esté de nuevo en el semiciclo positivo, tal como se puede observar en la siguiente figura, donde el pulso que dispara al SCR en cada semiciclo positivo es controlado por la acción del potenciómetro que regula la corriente y el condensador.

            p.mt-4.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 24] Control de disparo de un SCR a través de un resistor variable

            figure.mt-4
              img(data-aos="fade-up" src="@/assets/curso/tema4/3.svg")

        div(v-if="mostrar2")
          .p-5(style="background-color:#F3F9FF;border-radius:8px;" v-if="mostrar2" data-aos="fade-right")
            h4(data-aos="fade-up") Tiristor bidireccional TRIAC

            p.mt-4(data-aos="fade-up") Se trata de un tipo de tiristor, pero, a diferencia del SCR, este puede conducir en ambos sentidos; es decir que puede conducir tanto en el semiciclo positivo como en el semiciclo negativo. En esencia, un TRIAC es el juego de dos SCRs conectados en antiparalelo.

            p.mt-3(data-aos="fade-up") Como se puede observar en la  figura, por un lado, se tiene la estructura interna del TRIAC con los SCR en antiparalelo, y por otro, su símbolo esquemático, donde se observa un componente que puede conducir corriente en ambos sentidos y con un pin de compuerta que permite disparo del dispositivo en el instante que se requiera.

            p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 25] Tiristor TRIAC

            .bg-white.p-3.mt-4.col-md-7.m-auto(style="border: 1px #707070 solid")
                figure.mt-3
                  img(data-aos="fade-up" src="@/assets/curso/tema4/4.svg")

            figcaption.mt-3(data-aos="fade-up") Nota. a) Estructura interna del TRIAC con SCR en antiparalelo (b) Símbolo esquemático del TRIAC

            h4.mt-5(data-aos="fade-up") Control del ángulo de disparo TRIAC

            p.mt-4(data-aos="fade-up") Tal como sucede con el SCR, en el TRIAC es posible controlar el instante en que se dispara el TRIAC para que, al conectarlo a una fuente AC, se pueda controlar la potencia que se entrega a esta, ya que el TRIAC solo conducirá una porción de la onda senoidal, mas no la onda completa.

            p.mt-3(data-aos="fade-up") Como se puede observar en la siguiente figura, se tiene un circuito que está alimentando de manera controlada una lámpara en corriente alterna, al controlar el ángulo de disparo del TRIAC a través del circuito formado por la resistencia variable y el condensador, que controlan el disparo del mismo. En el oscilograma, se puede observar que a la carga solo se le está entregando la mitad de la potencia total, ya que el disparo del TRIAC, en cada semiciclo, se hace sobre los 90° de la señal.


            p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 26] Control de ángulo de disparo del TRIAC

            figure.mt-4
              img(data-aos="fade-up" src="@/assets/curso/tema4/5.svg")



</template>

<script>
import $ from 'jquery'
export default {
  name: 'Tema4',
  data: () => ({
    mostrarIndicador: true,
    modal1: false,
    mostrar1: true,
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
    eventoMostrar1() {
      this.mostrarIndicador = false
      this.mostrar2 = false
      this.mostrar1 = true
      $('.caja__1').addClass('caja__activa1')
      $('.caja__2').removeClass('caja__activa2')
    },
    eventoMostrar2() {
      this.mostrarIndicador = false
      this.mostrar1 = false
      this.mostrar2 = true
      $('.caja__2').addClass('caja__activa2')
      $('.caja__1').removeClass('caja__activa1')
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
.caja__activa1
  transition: transform .5s ease
  transform: scale(1.06)
.caja__activa2
  transition: transform .5s ease
  transform: scale(1.06)
.caja__activa1:after
  content: ''
  border-bottom: 13px transparent solid
  position: absolute
  right: -25px
  top: 42%
  border-left: 13px #b3009d solid
  border-right: 13px transparent solid
  border-top: 13px transparent solid
  width: 0
  height: 0
.caja__activa2:after
  content: ''
  border-bottom: 13px transparent solid
  position: absolute
  right: -25px
  top: 42%
  border-left: 13px #00cca7 solid
  border-right: 13px transparent solid
  border-top: 13px transparent solid
  width: 0
  height: 0
</style>
