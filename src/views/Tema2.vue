<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 2
      h1 Diodos

    p(data-aos="fade-up") El componente semiconductor más simple es conocido como diodo. Básicamente, es un dispositivo semiconductor hecho de la unión de dos semiconductores, uno tipo P y uno tipo N, dentro de un encapsulado. A esto se le conoce como la unión PN:

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 6]  Unión PN del diodo

    .row.mt-5.col-md-7.m-auto
      .col-md-6.p-0.mb-3
        h4.text-center(data-aos="fade-up") Tipo N
        figure.mt-2
          img(data-aos="fade-up" src="@/assets/curso/tema2/1.svg")

      .col-md-6.p-0.mb-3
        h4.text-center(data-aos="fade-up") Tipo P
        figure.mt-2
          img(data-aos="fade-up" src="@/assets/curso/tema2/2.svg")

      figure.mt-2.m-auto.text-center
          img.imagen_flotante_animada(data-aos="fade-up" src="@/assets/curso/tema2/3.svg" style="display:inline;width:60px;margin-top:-50px;")

      h4.text-center(data-aos="fade-up") Zona de deplexión

    p.mt-5(data-aos="fade-up") La frontera entre estos dos materiales se conoce como la #[strong zona de deplexión], y es allí donde la magia del funcionamiento de los semiconductores aparece por primera vez, ya que, de acuerdo con determinadas condiciones eléctricas de polarización y voltaje, el diodo se convierte en conductor o aislante, permitiendo o no la circulación de corriente a través de él.

    p.mt-4(data-aos="fade-up") Estas condiciones son básicamente dos, la primera es la polarización, es decir, el sentido en que se conecta una fuente de energía externa; y la segunda es que se requiere un mínimo de voltaje para lograr la conducción efectiva de los electrones dentro de esta unión PN; a este voltaje mínimo se le conoce como #[strong barrera de potencial], que típicamente, para un semiconductor como el germanio, ronda alrededor de los 0,3 V mientras que para el silicio está cerca de los 0,7 V.

    p.mt-4(data-aos="fade-up") Dependiendo de cómo se conecte la fuente externa al diodo, se tendrán dos polarizaciones posibles. Una es la polarización directa y otra es la polarización inversa, las cuales se pueden ver reflejadas en la siguiente figura.

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 7] Polarizaciones

    .row.mt-5.col-md-11.m-auto
      .col-md-6.mb-3
        figure.mt-2.m-auto.text-center
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/4.svg")
      .col-md-6.mb-3
        figure.mt-2.m-auto.text-center
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/5.svg")

    figcaption.mt-4.col-md-9 Nota. (a) Polarización inversa (b) Polarización directa

    p.mt-5(data-aos="fade-up") Como todo elemento que compone un circuito electrónico, el diodo tiene su respectivo símbolo, el cual puede visualizarse en la siguiente figura. También se puede observar cómo este se relaciona con la unión PN, además se puede ver su aspecto físico típico, aunque es necesario aclarar que no es el único.

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 8] Estructura y representación del diodo

    .row.mt-5
      .col-md-5.mb-3
        figure
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/6.svg")

      .col-md-1

      .col-md-3.mb-3(style="place-self: center;")
        figure
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/7.svg")

      .col-md-3.mb-3(style="place-self: center;")
        figure
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/8.svg")

    figcaption.col-md-6.mt-3(data-aos="fade-up") Nota. Nota. (a) Unión PN (b) Símbolo estandarizado (c) Aspecto exterior típico

    br
    br
    .titulo-segundo.mt-5
      h2#t_2_1 2.1. El diodo ideal

    p(data-aos="fade-up") Debido a las características propias del diodo como elemento semiconductor, se adoptan modelos específicos para el análisis que se hace de los diodos y su comportamiento en un circuito electrónico. El más simple es el conocido como diodo ideal, donde simplemente se determina que, dependiendo de la polarización del diodo, este conduce o no.

    p.mt-3(data-aos="fade-up") #[strong Un diodo ideal permite el paso de corriente en la condición de polarización directa, mientras que en la condición de polarización inversa se comporta como un elemento aislante, impidiendo el paso de corriente, tal como se diagrama en la siguiente figura.]

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 9] Efecto en la corriente dependiendo de la polarización del diodo ideal

    .row.mt-5.col-md-6.m-auto.p-3(style="background-color:#F8F8F8")
      .col-md-6.mb-3
        figure.mt-2.m-auto.text-center
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/9.svg")
        h4.mt-3.text-center(data-aos="fade-up") Hay flujo de corriente
      .col-md-6.mb-3
        figure.mt-2.m-auto.text-center
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/10.svg")
          h4.mt-3.text-center(data-aos="fade-up") No hay flujo de corriente

    p.mt-5(data-aos="fade-up") Si se asumen condiciones ideales en polarización directa, el diodo se comporta como corto, mientras que en polarización inversa se comporta como un circuito abierto.

    br
    br
    .titulo-segundo.mt-5
      h2#t_2_2 2.2. Circuitos con diodos

    p(data-aos="fade-up") Se debe tener en cuenta que ningún diodo se comporta de manera ideal, este elemento posee una serie de características eléctricas que determinan su comportamiento y aplicación. Es importante tenerlas en cuenta a la hora de seleccionar o reemplazar un diodo en un circuito.

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 10] Curva del diodo

    .col-md-9.mt-5.m-auto
      figure
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/11.svg")

    figcaption.mt-4.col-md-4 Nota. Nota. Adaptada de Arboledas, (2010)

    p.mt-5(data-aos="fade-up") Gracias a las características propias y el comportamiento de los diodos, se estudian una serie de circuitos típicos con diodos que constituyen sus aplicaciones más destacadas.

    p.mt-3(data-aos="fade-up") #[strong Existen al menos tres circuitos que se deben considerar en este aspecto.]

    .row.mt-5
      .col-md-4.mb-3
        .p-3(style="background-color:#F8F8F8;height:100%;border-radius:8px;")
          figure.mt-2.m-auto.text-center
            img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/12.svg")
          h4.mt-3.text-center(data-aos="fade-up") Rectificador de media onda
      
      .col-md-4.mb-3
        .p-3(style="background-color:#F8F8F8;height:100%;border-radius:8px;")
          figure.mt-2.m-auto.text-center
            img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/13.svg")
            h4.mt-3.text-center(data-aos="fade-up") Rectificador de onda completa con transformador de tap central

      .col-md-4.mb-3
        .p-3(style="background-color:#F8F8F8;height:100%;border-radius:8px;")
          figure.mt-2.m-auto.text-center
            img.image_floating(data-aos="fade-up" src="@/assets/curso/tema2/14.svg")
            h4.mt-3.text-center(data-aos="fade-up") Rectificador de onda completa con puente de diodos

    br
    br
    .titulo-segundo.mt-5
      h2#t_2_3 2.3. Diodos de propósito especial

    p(data-aos="fade-up") Existen varios tipos de diodos, dependiendo de su propósito. Su principio de funcionamiento, en esencia, es el mismo, pero cada cual tiene unas particularidades que le permiten trabajar en aplicaciones diferentes, dependiendo de las necesidades de cada circuito. Los más destacados se muestran a continuación:

    TabsC.color-primario.mt-5
      .py-3.py-md-4(titulo="Diodos rectificadores")
        .row
          .col-md-7.mb-4.mb-md-0
            h4 Diodos rectificadores
            p.mt-3 Los diodos rectificadores están destinados a los circuitos rectificadores, específicamente, cuyo propósito es convertir corriente alterna en continua. Básicamente, se trata de un diodo simple que funciona, tal como se expuso anteriormente: en polarización directa, conduce; y en polarización inversa, no conduce.

            p.mt-4 Estos se subdividen en diodos rectificadores de propósito general (a veces llamados de señal) y diodos rectificadores de potencia. Su diferencia principal radica en sus capacidades de conducción y obviamente en su tamaño.
        
          .col-md-5
            p.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 12] Tipos de diodos rectificadores
            figure
              img(src='@/assets/curso/tema2/15.svg', alt='')

      .py-3.py-md-4(titulo="Diodos Zener")
        .row
          .col-md-7.mb-4.mb-md-0
            h4 Diodos Zener
            p.mt-3 Los diodos Zener son un tipo de diodo cuya función usualmente es regular el voltaje, ya que en polarización directa se comporta como un diodo convencional, permitiendo el paso de corriente si se supera su voltaje umbral, mientras que en polarización inversa, a pesar de que el diodo no conduce, sí mantiene un voltaje constante; es decir, mantiene regulado un valor de voltaje determinado que depende específicamente de la referencia del diodo. 

            p.mt-4 Esta particularidad en la región inversa de su curva se puede observar en la siguiente figura, donde el voltaje en polarización inversa queda fijo en un voltaje determinado, que en este caso particular es de 8 V. Existen comercialmente muchas referencias de diodos Zener, se resaltan típicamente diodos de 3,3 V, 5 V, 5,6 V y 12 V, por mencionar algunos.
        
          .col-md-5
            p.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 13] Curva del diodo Zener
            figure
              img(src='@/assets/curso/tema2/16.svg', alt='')

      .py-3.py-md-4(titulo="Diodos LED")
        .row
          .col-md-7.mb-4.mb-md-0
            h4 Diodos LED
            p.mt-3 Podría decirse que estos diodos cambiaron la manera como presentamos la información de un sistema electrónico y han tenido desde su creación varios avances. Los LED no son otra cosa que diodos que con polarización directa emiten un haz de luz de un color específico, dependiendo del dopaje de su semiconductor; en inversa, los LED simplemente no encienden, pero hay que tener precaución porque, como todo diodo, tienen sus límites de voltaje en inversa y de corriente en directa.

            p.mt-4 En la siguiente figura, se puede observar el aspecto físico de los mismos y su encapsulado típico, pero no es el único con el desarrollo de los mismos para la iluminación de espacio o como indicadores en equipos electrónicos como celulares, tablets, TV, etc. Sus encapsulados son muy variados en forma y tamaño.
        
          .col-md-5
            p.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 14] Encapsulado típico de los diodos LED
            figure
              img(src='@/assets/curso/tema2/17.svg', alt='')

        .row.mt-5
          .col-md-7.mb-4.mb-md-0
            p.mt-3 En los diodos led, la barrera umbral para que el diodo conduzca y produzca su haz de luz característico no se produce a un valor tan bajo como los 0,7 V. Esto depende del color del diodo, ya que para producir los diferentes colores es necesario usar una impureza para dopar el semiconductor diferente. En la siguiente tabla, se presentan los valores típicos de tensión de operación del diodo, dependiendo de su color:

            p.mt-4 Hay que tener en cuenta que estos valores son los típicos para los diodos indicadores. Los diodos de potencia manejan algunos valores tanto en corriente como en voltaje superiores, ya que en promedio los leds mencionados en la tabla anterior consumen alrededor de 20mA. Un diodo de potencia, dependiendo de sus características, podría llegar a consumir hasta 500mA.
        
          .col-md-5
            p.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Tabla 1]  Cuadro de clasificación del diodo según color
            figure
              img(src='@/assets/curso/tema2/18.svg', alt='')

    figcaption.mt-4.col-md-5(data-aos="fade-up") Nota. Imágenes Tomadas de Arboledas (2010, p. 90)



</template>

<script>
export default {
  name: 'Tema2',
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
</style>
