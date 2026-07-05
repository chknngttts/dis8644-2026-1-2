# examen-grupo-01

## integrantes

- Benjamín Alonso Álvarez Pavez / [benjaminalvarez21](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/03-benjaminalvarez21>)
- Anays Valentina Cornejo Candia / [Anaysval](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/09-Anaysval>)
- Bruno Ferrari Meyer / [chknngttts](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/11-chknngttts>)
- Lucas Ignacio Ortiz Aguirre / [ryukivol](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/21-ryukivol>)
- Nicolás Elías Valdés Greve / [nicolasvaldesgreve](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/31-nicolasvaldesgreve>)

## criterios de diseño del sistema

### de donde partimos?

No teniamos conocimientro previo antes de entrar al taller, fue nuestra primera vez trabajando con y soldando componentes electronicos a placas. Aparte de las clases que dieron los profesores buscamos inspiración en paginas web como foros y canales de youtube que mostraban como hacer partes de sintetizadores (ej; filtros, amplificadores, reguladores etc...).

Todo este proceso ha sido prueba y error, si no funciona, se cambia y se vuelve a intentar. Gran parte de la ayuda fue entre compañeros, nos apoyamos para arreglar problemas comunes, compartíamos datos de lugares de compra y paginas web para buscar circuitos interesantes.

------------

## referentes

### WhiteSample

artista chileno que usa sintetizadores analógicos

ha trabajado con lollapalooza con estructuras interactivas (WhiteSample, 2014)

su música es experimental/electrónica

![whitesample](./imagenes/whitesample-2.jpg) (WhiteSample & Cargo Collective, 2012)

-------------

### anthony1

dj/productor chileno

ha hecho tocatas ambientales donde utiliza sintetizadores analogicos y efectos digitales

forma parte de un colectivo de varios artistas electronicos chilenos (Team Mekano)

![anthony1](./imagenes/anthony1.png) (Anthony1, 2022)

----------------

## disponibilidad material

en cuanto a la disponibilidad material en chile nos ubicamos principalmente en 2 lugares/tienda; *San Diego* y *Victronics*. en *San Diego* se encuentran varias tiendas de electronicas que ofrecen distintos componentes, la gracia es los distintos lugares y sus especialidades.

*Victronics* es una tienda online, por eso pueden ofrecer precios más bajos, además tienen accesorios como espaciadores y pernos para armar las carcasas.

### BOM PCB MAINCRA

Este módulo te permite interactuar con el sintetizador mediante vibraciones en el piezo, mediante golpes en el mismo. Estas vibraciones serás captadas por el piezo, lo cual lo tomará como señal para avanzar en el secuenciador.

La idea detrás de esta propuesta nace de la posibilidad de sentir y ver las vibraciones. Aquello que parece caótico o insignificante puede contener señales que, al prestar suficiente atención, adquieren un significado propio. Siguiendo esa lógica, el piezo actúa como un medio para captar esas vibraciones y convertirlas en acciones dentro del sintetizador, permitiendo que elementos normalmente invisibles se vuelvan parte de la interacción.

| Componente | Cantidad | PCB | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- | --- |
| Chip NE555P | 1 | U1 | $490 | <https://www.victronics.cl/circuitos-integrados/lm555cngeneralpurposebipolartimerdip8/> | Sí |
| Chip TL072CP | 1 | U4 | $990 | <https://www.victronics.cl/circuitos-integrados/tl072cpdualjfetlowpoweropamplifierdip8/> | No |
| Regulador L7805CV | 1 | U3 | $350 | <https://www.victronics.cl/reguladores/reguladorvoltl7805cv5v-15ato220/> | No |
| Diodo 1N4007 | 1 | D5 | $200 | <https://www.mechatronicstore.cl/diodo-rectificador-in4007-1n4007-4007/> | Sí |
| Diodo 1N5819 | 2 | D6, D7 | $586 | <https://cl.rsdelivers.com/product/nexperia/bat85113/nexperia-diodo-bat85113-diodo-schottky-200-ma-30-v/0300978> | No |
| Transistor 2N2222 | 1 | Q1 | $200 | <https://www.mechatronicstore.cl/transistor-2n2222/> | Sí |
| Potenciómetro B10K | 1 | RV1 | $495 | <https://altronics.cl/potenciometro-lineal-10k-b10k> | No |
| Potenciómetro B500K | 1 | RV2 | $495 | <https://altronics.cl/potenciometro-lineal-500k-b500k?search=b500k> | Sí |
| LED 3mm | 3 | D1, D2, D8 | $100 | <https://www.mechatronicstore.cl/led-3mm-5mm/> | Sí |
| Resistencia 47 Ω | 1 | R12 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | No |
| Resistencia 100 Ω | 1 | R18 |  $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 220 Ω | 1 | R14 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 1 KΩ | 6 | R1, R3, R6, R7, R8, R11 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 2,2 KΩ | 1 | R13 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | No |
| Resistencia 10 KΩ | 2 | R4, R5 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 100 KΩ | 3 | R2, R16, R17 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 2,2 MΩ | 1 | R15 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | No |
| Condensador cerámico 1 µF | 1 | C9 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 4.7 nF | 1 | C12 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 10 nF | 1 | C13 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 100 nF | 3 | C1, C7, C10 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | Sí |
| Condensador polarizado 10 µF | 2 | C9, C11 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Condensador polarizado 100 µF | 3 | C2, C3, C5 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Piezo | 1 | J8 | $990 | <https://www.mechatronicstore.cl/sensor-piezoelectrico-27mm-con-cable/> | Sí |
| Cables dupont 40 uni. | 1 | - | $2.990 | <https://mcielectronics.cl/shop/product/cable-dupont-macho-macho-20cm-pack-40-unidades-2/> | Sí |
| Batería 9V recargable | 1 | BT1 | $7.990 | <https://www.sodimac.cl/sodimac-cl/articulo/110251085/bateria-recargable-9v/110251089> | Sí |
| Interruptor Switch | 1 | SW3 | $570 | <https://www.katode.cl/switches/1339-interruptor-switch-2-pines-on-off-corto.html?> | No |

### BOM PCB 02, GRUPO 02: REGISTRO DE DESPLAZAMIENTO ESTÁTICO / NYAN CAT

Este circuito también se categoriza como un secuenciador, es decir, que genera corrientes eléctricas en un patrón repetitivo y ordenado. Podemos tomar el mismo ejemplo del semáforo mencionado en el circuito anterior, donde este funciona encendiendo un LED detrás del otro sucesivamente hasta que se repite el ciclo.

Adicionalmente funciona con el mismo corazón, es decir un reloj que alimenta a este secuenciador. Este nos va a definir la velocidad con la que avanza la ola. Este secuenciador entrega distintas salidas o compases en el orden ya mencionado. El como ocurre esto es muy llamativo, ya que el cerebro detrás de todo esto, realmente son 2, los que se comunican entre ellos para poder generar el efecto ola o cascada.

| Componente | Cantidad | PCB | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- | --- |
| Chip 4015 | 1 | U2 | $1.400 | <https://www.mactronica.com.co/cd4015?> | No |
| Regulador L7805CV | 1 | U4 | $350 | <https://www.victronics.cl/reguladores/reguladorvoltl7805cv5v-15ato220/> | No |
| Transistor 2N2222 | 8 | Q3, Q4, Q5, Q6, Q7, Q8, Q9, Q10 | $220 | <https://www.cabezacuadrada.cl/product/pn2222a/> | Sí |
| Transistor BC548 | 1 | Q1 | $200 | <https://www.mechatronicstore.cl/transistor-bc548/?> | No |
| LED 3mm | 9 | D1, D2, D3, D4, D5, D6, D7, D8, D12 | $100 | <https://www.mechatronicstore.cl/led-3mm-5mm/> | Sí |
| Resistencia 220 Ω | 8| R4, R5, R6, R7, R8, R9, R10, R11 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 1 KΩ | 18 | R3, R12, R15, R16, R17, R18, R19, R20, R21, R22, R23, R24, R25, R26, R27, R28, R29, R30 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 10 KΩ | 1 | R2 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Resistencia 100 KΩ | 1 | R13 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Diodo 1N4007 | 1 | D11 | $200 | <https://www.mechatronicstore.cl/diodo-rectificador-in4007-1n4007-4007/> | Sí |
| Condensador cerámico 100 nF | 1 | C9 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | Sí |
| Condensador polarizado 10 µF | 1 | C8 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Condensador polarizado 100 µF | 1 | C7 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Interruptor Switch | 1 | SW4 | $570 | <https://www.katode.cl/switches/1339-interruptor-switch-2-pines-on-off-corto.html?> | No |

### BOM PCB 03, GRUPO 03: COMANDO ESTELAR

Este módulo recibe dos inputs, energía eléctrica a través de los conectores barrel jack y el voltaje de control que se ajusta girando el potenciómetro RV1, el cual determina la frecuencia de oscilación. Internamente ese voltaje entra al chip CD4046, el centro del circuito, que lo convierte en una oscilación cuya velocidad varía según ese voltaje. Esa señal pasa luego por dos inversores CD40106 que la limpian y estabilizan, hasta llegar al conector de audio jack (J4), que es el output del módulo, una señal oscilante limpia y lista para ser procesada por los demás módulos del sintetizador.

| Componente | Cantidad | PCB | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- | --- |
| Chip CD4046 | 1 | U1 | $700 | Electrónica Real | |
| Chip CD40106 | 1 | U4 | $1200 | Electrónica Real | |
| L7805 | 1 | U2 | $350 | Victronics | |
| Diodo 1N4007 | 1 | D1 | $790 | Victronics | |
| LED | 1 | D2 | $920 | Electrónica Real | |
| Resistencia 100kΩ | 1 | R1 | $890 | Electrónica Real | |
| Resistencia 1kΩ | 1 | R2 | $890 | Electrónica Real | |
| Potenciómetro 100Ω | 2 | RV1, RV2 | $500 | Afel a Ingeniería | |
| Capacitor 10nF | 1 | C1 | $520 | Victronics | |
| Capacitor 100nF | 1 | C5 | $500 | Victronics | |
| Capacitor 100uF | 2 | C2, C6 | $670 | Victronics | |
| Capacitor 10uF | 2 | C3, C4  | $330 | Victronics | |
| Capacitor 1uF | 1 | ?? | $300 | Victronics | |
| Jack DC | 2 | J2, J3 | $150 | Electrónica Real | |
| Jack de audio | 1 | J1 | $150-$300 | Victronics | |

Soldado 6 Horas

 Según yo esto no va

| Interruptor de palanca SPDT ON-ON | 1 | SW1 | $590 | Electrónica Real | |
| Separador o tornillo de montaje (M3*8) | 4 | 4 | $54 | Pernos Alameda | |
| Cable Dupont | 19 | 19 | $1190 (pack 10) | MCI Electronics | |

----------------

nombre de sistema/instrumento construido por medio de módulos

??? AL FINAL PONER ESTO

----------------

# **placas soldadas**

principio de funcionamiento de cada una, qué tipo de señal entrega a la salida, qué recibe
lista de materiales con costos. Incluir tiempo de soldadura

Nuestro sintetizador está formado de 4 modulos:

## maincra (Piezo/entrada)

*un microfono de contacto que detecta vibraciónes, manda señales a un amplificador e inversor de señales. estos convierten la corriente la cual entra a un reloj interno que lo camba a pasos para que un sequenciador pueda funcionar.*

## nyan cat (Sequenciador)

*un sequenciador de 8 pasos (y dos fases) que permite la conexión de multiples osciladores.*

## comando estelar (Oscilador)

*esta placa utiliza 2 chip para general oscilaciónes que alteran a traves de potenciómetros que permiten cambiar tanto la frecuencia como la modulación del sonido.*

## parla (Amplificador/Salida)

*es un amplificador de señal que permite escuchar las oscilaciónes del modulo anterior con mayor volumen.*


-------------

## procesos

![test](./imagenes/procesos-largo.png)

![test gif-1](./imagenes/corte-laser-1.gif) ㅤㅤㅤㅤㅤㅤㅤ ![test gif-2](./imagenes/grito-test-medio.gif)

#### para tener un flujo de trabajo más ordenado pusimos todos los conmponentes necesarios para armar una placa de lado.

> 1era dificultad
>
> tuvimos problemas con la organización en la compra de componentes, listas incompletas
>

#### soldamos los componentes por tamaño (de más pequeño a más grande) y cables para los que van montados en la carcasa.

> 2da dificultad
>
> también tuvimos problemas con el corte del acrílico para la carcasa
>
> 1er corte: falta de agujeros para componentes y tamaño equivocado
>
> 2do corte: formato no compatible de archivo
>
> 3er/4to/5to corte: parametros erroneos y líneas de corte extra
>
> 6to corte: por falta de material usamos los restantes de cortes anteriores

#### armamos las carcasas con los separadores

> 3era dificultad
>
> falta de separadores para las carcasas por modificaciones en tamaño
>

#### al tener todo soldado en la placa se empezó a armar la cubierta de acrílico con los separadores (gracias al grupo 0X por darnos sus separadores restantes), pusimos los potenciómetros, entradas/salidas de audio y switch conectados con los cables

> 4ta dificultad
>
> funcionamiento correcto de las PCB, soldamos varias veces las placas, cambiamos los componentes y remplazamos los cables pero no funcionaban.
>

----------------

## carcasa

decisiones materiales y formales de la carcasa
inspiración y referentes (con cita)

> *escogimos trabajar con acrilico ya que eramos familiares con el material. es fácil de trabajar por su compatibilidad con el corte laser que nos permitía cortar varias carcasas, grabar y lograr un buen oficio. el material es firme, perfecto para lo que teniamos en mente, además es economico.*
>
> *una cualidad del acrílico que utilizamos es la transparencia. buscamos celebrar el diseño de las PCB a través de la transparencia de este, rompiendo la caja negra e invitando a la apreciación integral de cada placa y sus distintos componentes.*

### referentes carcasa

> para la carcasa usamos estos 3 ejemplos:
>
> cmf phone - Nothing (Nothing, 2024)
>
> microKorg crystal - Korg (KORG, 2022)
>
> gameboy transparente - Nintendo (Amo, 2011)
> 

## composición

### Referentes

- **Yoko Ono:**

> ### **"pieza de escondite"**
>
> *"esconderse hasta que todos se vayan a sus casas."*
>
> *"esconderse hasta que todos se olviden de uno."*
>
> *"esconderse hasta que todos todos se mueran"*
> *(Ono, 1964, 25)*

??? 1 MAS

---

#### Integración a la vida diaria

Al hacer brainstorming de que podriamos hacer como partitura nos dimos cuenta que nuestras ideas eran actividades que independientes de nuestra partitura se llevan a cabo. Nosotros nos introducimos a esta creando una composición nueva cada vez que se toca. 

---

#### Ping Pong

*(ver. literal 2)* **Como grupo-01 vamos a ir a República 180, Santiago de Chile con “maincra” (piezo-01), el parlante, “nyan cat” (secuenciador-2) y "comando estelar" (oscilador-1). Pedir las paletas y pelotas donde los guardias. Pondremos un piezo en cada paleta de ping pong con masking tape. Situar el sintetizador bajo la mesa, asegurar que los cables no se enreden entre sí. Jugar una partida completa de Ping Pong de 21 puntos, con el impacto de la pelota en las paletas el secuenciador avanza, haciendo que el oscilador pueda funcionar. Al terminar la partida devolver las paletas y pelota a los guardias.**

*(ver. poética)*

>**Ve a República 180 y ubica el piezo en la mesa de ping pong**

>**Invita a alguien a jugar**

>**Jueguen durante 5 minutos o hasta que se aburran**

------------------



-----------------

## bibliografía

PEGAR DEL DOC YA ESTAN CASI TODAS

-----------------

## preguntas domingo

```
placas usadas:

- placa 01: piezo, diseñada por grupo 01
- placa 02: secuenciador, diseñada por grupo 02
- placa 03: oscilador, diseñada por grupo 03

explicación de flujo de señal de audio:

ordenado a grandes rasgos gesto humano a fuentes de tiempo, a secuenciador, a osciladores, a filtros, a mezcladores, a parlante

- la placa 01 es el piezo, tiene como entrada un golpecito en el piezo, y la salida es un pequeño voltaje que va conectado a la placa 02 secuenciador.
- la placa 02 tiene como entrada la señal de control del piezo, estamos viendo como arreglaralo ya que la primera vez no funcionó. estamos soldando uno nuevo para ver si fue un error de soldadura con nuevos componentes. de las 8 entradas usamos 4, jel 4to siendo reset para comenzar el ciclo de nuevo. (soldamos el pin 2 y 14 como una forma de hechizo)
- cada placa 03 de osciladores es una fuente sonora, tenemos 3 montados juntos en una carcasa. tuvimos un problema con la placa del medio, nunca sonaba correctamente. soldamos uno ultimo y nos dimos cuenta que usamos un chip erroneo y una cama estaba mal puesta.

estado de construcción:
- placa 01: no funciona, la entrada original del piezo no es funcional, si uno se conecta al otro audiojack se prenden LEDs. los potenciometros controlan la intensidad de la luz y bloquean al piezo.
- placa 02: no funciona, las LEDs no se prenden junto a los steps (el grupo del secuenciador nos contó que tambíen encontraron este error en la protoboard y que no affecta realmente el funcionamiento de los steps). 
- placa 03: funcionan algunos, los de los costados suenan correctamente, el del medio tiene más problemas. nos dimos cuenta que pusimos mal una cama/zapato y que usamos un chip distinto al resto. ahora estamos soldando los componentes nuevamente con el chip correcto.

ayudas eléctricas que necesitamos domingo:

- placa 01: queremos ayuda viendo las conexiónes del piezo. ver como hacerlo funcionar correctamente.
- placa 02: vamos a preguntar a compañeros primero y si no ver temas de LEDs y confirmar buen funcionamiento
- placa 03: ver tema placa del medio. 

ayuda audio que necesitamos domingo:

- ver conexión placas entrada/salida. ver como conectar todos los osciladores a un parla

materiales faltantes:

- chip 4046 40106 para grito (para tener a mano por si algo se quemara)
