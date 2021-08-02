<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal
      .titulo-principal__numero
        span 3
      h1 Transistores

    p(data-aos="fade-up") La invención del transistor marcó un hito en la evolución de la tecnología en el siglo XX, pues, gracias a él, se avanzó a pasos agigantados en muchas áreas de la ingeniería, como las telecomunicaciones y la informática, pudiendo miniaturizar muchos equipos y sistemas electrónicos que hasta ese momento eran de considerables proporciones.

    .bloque-texto-a.color-primario.p-4.p-md-5.mt-5.caja_flotante(data-aos="fade-left")
      .row.m-0.align-items-center.justify-content-between
        .col-lg-4.mb-4.mb-lg-0
          
        .col-lg-8
          .bloque-texto-a__texto.p-5.caja_escalada_hover(style="background-color: rgb(255 255 255 / 95%);")
            p(data-aos="fade-up") Un transistor es un elemento semiconductor que posee tres terminales: dos por donde transita la corriente y una tercera que se considera de control.

    br
    br
    .titulo-segundo.mt-5
      h2#t_3_1 3.1 El transistor BJT

    p(data-aos="fade-up") También conocidos como transistores bipolares. Los transistores BJT están formados por tres capas de semiconductor y, dependiendo de la conformación de estas capas, hay dos tipos de transistores BJT: uno es el que está conformado por dos capas N y una en medio P, conocido como transistor tipo NPN; el segundo es el conformado por dos capas tipo P y una en el centro de tipo N, también conocido como transistor PNP. La capa de la mitad de cualquiera de los dos recibe el nombre de ‘base’ y sus extremos son conocidos como ‘emisor’ y ‘colector’.

    p.mt-5.p-1(data-aos="fade-up" style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 15]  Tipos de transistores

    .col-md-7.mt-5.m-auto
      figure
          img.image_floating(data-aos="fade-up" src="@/assets/curso/tema3/2.svg")

    figcaption.mt-4.col-md-3 Nota.  (a) Tipo NPN (b) Tipo PNP

    h5.mt-5(data-aos="fade-up") A continuación, se presentan los modos de trabajo del transistor.

    AcordionA.mt-5(tipo="a" clase-tarjeta="tarjeta tarjeta--azul")
      .row.p-4(titulo="Polarización del transistor")
        .col-md-12.mb-4.mb-md-0
          p Según Arboledas (2010): “en un transistor, existen dos uniones PN: una entre emisor y base (EB) y otra entre base y colector (BC). Estas uniones deben polarizarse de tal modo que la unión EB se polarice directamente y la unión BC inversamente”. Esta polarización se puede observar en la figura. 

        .col-md-6.mt-5
          p.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 16] Polarización de un transistor NPN
          figure.mt-3
            img(src='@/assets/curso/tema3/3.svg', alt='')
            figcaption.mt-2 Nota. Tomada de Arboledas (2010, p.98).

        .col-md-12.mt-5
          p Al polarizar el transistor, se producen tres corrientes: una, la que ingresa por el terminal de base o corriente de base (IB), está la corriente de colector (IC) y la tercera es la corriente de emisor (IE), que realmente es la resultante de la suma de la corriente de base más corriente de colector; y son las corrientes las protagonistas en el funcionamiento del transistor, ya que al inyectar una pequeña corriente de base en el transistor se consigue que el transistor conduzca una gran corriente de colector, de tal forma que resulta en un pin de control. El pin de base de la corriente ingresa por el colector y sale por el emisor sumada a la pequeña corriente de base.

        //.row.col-md-10.p-3.mt-5(style="background-color:#00CCA7;border-radius:10px;")
          .col-md-8(style="place-self: center;")
            h5.mb-0 El transistor como interruptor
          .col-md-4(style="text-align:right;")
            a.boton.boton--b.color-acento-botones(@click="modal1 = true") Ver contenido
        
        //ModalA(:abrir-modal.sync="modal1")
          .p-3
            h4 El transistor como interruptor
            p.mt-4 Con base en el análisis de las corrientes y las caídas de voltaje asociadas a las cargas o resistencias presentes en un circuito típico de transistor, se tienen ciertas relaciones matemáticas de estas que se pueden observar a continuación.

            p.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 17]  Relación de corrientes y voltajes en un circuito con transistor BJT tipo NPN.
            figure.mt-3.col-md-10.m-auto
              img(src='@/assets/curso/tema3/13.svg', alt='')


      .row.p-4(titulo="El transistor como interruptor")
        .col-md-12
          p.mt-4 Con base en el análisis de las corrientes y las caídas de voltaje asociadas a las cargas o resistencias presentes en un circuito típico de transistor, se tienen ciertas relaciones matemáticas de estas que se pueden observar a continuación.

          p.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 17]  Relación de corrientes y voltajes en un circuito con transistor BJT tipo NPN.
          figure.mt-3.col-md-10.m-auto
            img(src='@/assets/curso/tema3/13.svg', alt='')

          p.mt-5 Dependiendo de la relación entre el voltaje de colector emisor versus su corriente de colector resultante de la corriente de base que se inyecta, se puede determinar lo que se conoce como la zona de trabajo del transistor, de la cual pueden distinguirse al menos tres zonas de trabajo:

          p.mt-4 #[strong Zona activa,] en la cual el transistor tiende a amplificar la señal resultante gracias al efecto de la relación de corrientes.
          
          p #[strong Zona de saturación,] donde el transistor está en la capacidad de conducir la mayor corriente posible.
          
          p #[strong Zona de corte,] que, como su nombre lo indica, es donde la corriente no circula, está cortada.
      
        .col-md-12.mt-5
          p.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 18] Zonas de trabajo del transistor BJT.
          figure.col-md-5.m-auto.mt-4
            img(src='@/assets/curso/tema3/14.svg', alt='')
            figcaption.mt-2 Nota. Tomada de Aranzabal, (2001).

        .col-md-12.mt-5
          p Cuando el propósito es usar el transistor como un interruptor, el transistor estará operando entre las zonas de saturación y corte, de tal manera que la base del transistor tendrá un circuito o elemento, sensor, etc., que le permitirá regular su corriente lo suficiente para hacer que pase de un estado a otro, de conducir mucha corriente, comportándose como un interruptor cerrado, a que no pase prácticamente ninguna corriente, comportándose como un interruptor abierto.

          p.mt-5.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 19] Representación de los efectos eléctricos en un circuito producto en las zonas de corte y saturación de un transistor

          .row.mt-5.col-md-11.m-auto
            .col-md-12
              figure
                img(src="@/assets/curso/tema3/15.svg")
            .col-md-4.mb-3
              h4.mt-3.text-center Representación esquemática del circuito

            .col-md-4.mb-3
              h4.mt-3.text-center Representación del efecto en el circuito de un transistor en zona de corte 

            .col-md-4.mb-3
              h4.mt-3.text-center Representación del efecto en el circuito de un transistor en zona de saturación

          p.mt-4 En la industria, los transistores son ampliamente usados como interruptores en fuentes drivers de motores y demás. Es posible encontrar miles de millones de ellos encapsulados, trabajando en conjunto, en los procesadores modernos, donde trabajan como interruptores, cerrando y abriendo circuitos a grandes velocidades. En un procesador, un transistor en corte representa un «cero lógico» o binario, y un transistor en saturación representa un «uno lógico» o uno binario.


      .row.p-4(titulo="El transistor en zona activa")
        .col-md-12
          p Esta zona se utiliza para amplificar señales de voltaje alterno. Existen varias configuraciones de amplificadores construidos a base de transistores BJT, pero en general se recomienda siempre que en un circuito con un solo transistor se agregue a la polarización una resistencia entre el emisor y la tierra del circuito, es decir, una resistencia de emisor.

          p.mt-3 Un ejemplo típico de este tipo de circuitos es un amplificador de emisor común con polarización por divisor de voltaje. Se le llama así porque el emisor resulta común para la referencia de la fuente alterna que inyecta la señal AC al circuito y su polarización de base se obtiene configurando un divisor de tensión que proporciona la corriente de base indicada para poner al transistor en la zona activa. Se puede observar el circuito en la siguiente figura.

          p.mt-5.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 20] Circuito típico de un amplificador en emisor común

          figure.mt-3
            img(src="@/assets/curso/tema3/9.svg")
          figcaption.col-md-6.mt-3 Nota.  (a) Esquemático del amplificador (b) Oscilograma resultante.

    br
    br
    .titulo-segundo.mt-5
      h2#t_3_2 3.2 Transistor MOSFET

    p(data-aos="fade-up") Los transistores MOSFET han ido reemplazando a los transistores bipolares en ciertos campos donde estos no resultaron tan eficientes. MOSFET (#[em Metal-Oxide-Semiconductor Field-Effect Transistor], en inglés) es un transistor de efecto de campo metal-óxido-semiconductor. Este se diferencia del BJT porque no trabaja con la inyección de corriente en su pin de control, sino que depende de un nivel específico de voltaje, que genera un campo eléctrico, que le permite a este elemento semiconductor conducir corriente.

    p.mt-3(data-aos="fade-up") Un transistor MOSFET cuenta con tres terminales: una es el surtidor, por donde generalmente ingresa la corriente que puede conducir el transistor cuando está correctamente polarizado; esta corriente pasa y sale por el drenador, que es la segunda; este paso de corriente es controlado por la compuerta, que es la tercera terminal y funciona como control de este dispositivo.

    p.mt-3(data-aos="fade-up") Hay dos tipos de MOSFET, dependiendo de cómo está construido el semiconductor que forma la compuerta y el resto del transistor.

    p.mt-4(data-aos="fade-up") #[strong En la siguiente figura se pueden observar los tipos de MOSFET.]

    p.mt-5.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 21] Tipos de MOSFET.

    .row.mt-5.col-md-11.m-auto
      .col-md-6
        .p-5.caja_flotante.caja__mostrar(style="background-color:#B3009D;border-radius:7px;height:100%;cursor:pointer;" @mouseover="eventMostrar1" v-if="!mostrar1")
          h3.text-white.text-center(data-aos="fade-up") MOSFET de canal N

          p.mt-5.text-white(data-aos="fade-up") Este se activa cuando se le proporciona un voltaje positivo, así como la polarización del terminal del drenador también debe ser positiva, eso sí, limitada por una resistencia. El surtidor, por su parte, debe encontrarse polarizado de manera negativa. Su símbolo esquemático puede verse en la imagen, teniendo como característica que posee una flecha apuntando hacia la compuerta.

        .p-5.caja_flotante.caja__mostrar(style="background-color:#F6F6F6;border-radius:7px;height:100%;cursor:pointer;" v-if="mostrar1" @mouseleave="eventSalir1")
          h3.text-center MOSFET de canal N
          
          figure.mt-5
            img.imagen_flotante_animada(src="@/assets/curso/tema3/10.svg")


      .col-md-6
        .p-5.caja_flotante.caja__mostrar(style="background-color:#3C0061;border-radius:7px;height:100%;cursor:pointer;" @mouseover="eventMostrar2" v-if="!mostrar2")
          h3.text-white.text-center(data-aos="fade-up") MOSFET de canal P

          p.mt-5.text-white(data-aos="fade-up") Consiste en un transistor cuya compuerta debe ser activada con un voltaje negativo respecto a tierra. En este caso, se debe polarizar con voltaje positivo el surtidor, y el drenador debe estar polarizado a tierra con una resistencia que ayude a limitar la corriente que circula. En su símbolo esquemático se puede distinguir porque cuenta en la compuerta con flecha que va hacia afuera.

        .p-5.caja_flotante.caja__mostrar(style="background-color:#F6F6F6;border-radius:7px;height:100%;cursor:pointer;" v-if="mostrar2" @mouseleave="eventSalir2")
          h3.text-center MOSFET de canal P

          figure.mt-5
            img.imagen_flotante_animada(src="@/assets/curso/tema3/11.svg")

    p.mt-5(data-aos="fade-up") Al igual que con el transistor BJT, el MOSFET es ampliamente utilizado como un interruptor controlado eléctricamente, por lo cual también cuenta con una condición de saturación que le permite comportarse como un interruptor cerrado.

    p.mt-5.p-1(style="padding-left:13px !important;border-left:4px #FFD947 solid;") #[strong Figura 22] El transistor MOSFET en conmutación
    
    figure.col-md-9.m-auto.mt-5
      img.image_floating(data-aos="fade-up" src='@/assets/curso/tema3/12.svg', alt='')
    
    figcaption.col-md-8.mt-3(data-aos="fade-up") Nota.  (a) En zona de saturación (b) En zona de corte. Tomada de tutoriales de electrónica básica (s. f.).

    h5.mt-5(data-aos="fade-up") Para lograr esa característica se deben cumplir algunas condiciones en la polarización:

    .cajon.color-primario.p-5.mt-5.caja_flotante_azul
      ol.lista-ol--cuadro
        li(data-aos="fade-up") 
          .lista-ol--cuadro__vineta
            span 1
          |  El voltaje entre compuerta y surtidor VGS es mayor que el voltaje umbral, esto quiere decir que, para cada referencia de MOSFET, existe establecido un voltaje VGS mínimo para lograr la polarización y este debe ser superado para poner el transistor en saturación.
        
        li.mt-3(data-aos="fade-up")
          .lista-ol--cuadro__vineta
            span 2
          |   El surtidor debe estar conectado a una fuente de voltaje positivo. En estas condiciones, el voltaje de drenaje a surtidor tiende a ser cero VDS=0, esto debido a que el transistor entra en la conocida región óhmica, donde la resistencia interna del dispositivo suele ser muy baja, permitiendo que pase la mayor corriente de drenador posible.

    p.mt-5(data-aos="fade-up") Las características propias de cada transistor MOSFET se pueden consultar en las hojas características del fabricante, donde se puede conocer el VGS necesario para la activación del transistor, así como la resistencia en la zona óhmica RD que permite calcular el voltaje mínimo entre drenador y surtidor en estas condiciones.





</template>

<script>
export default {
  name: 'Tema3',
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
.bloque-texto-a.color-primario
  background: url("../assets/curso/tema3/1.svg")
.bloque-texto-a:before
  left: 44% !important
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
.lista-ol--cuadro__vineta
  background-color: #00CCA7
</style>
