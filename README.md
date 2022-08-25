# proyectoAmbientesComputacionales

#Disenio

### Seleccion de paleta de colores
* [AdobeColor](https://color.adobe.com)
* [Colors](https://coolors.co/app)
* [Hacer degradados css](http://www.cssmatic.com/)


#HTML

#CSS
###Pseudoclases
* selector:hover : Se activa cuando el puntero esta sobre

* selector:active : Funciona cuando precionamos el elemento

* selector:visited : Cambia las propiedades de algo que hayamos visitado

* selector:nth-child(1) : Selecciona en la lista de "selectores" el numero que se especifica.


###Pseudoelementos
Permiten seleccionar ciertos elementos del html

* selector::first-line : seleccion a la primera linea de un parrafo

* selector::first-letter : selecciona la primera letra.

* selector::selection : Especifica los estilos para el texto cuando es seleccionado

* selector::before : permite anadir contenido antes del elemento. con la etiqueta `content: 'Esto es un elemento'`

* selector::after : permite anadir contenido despues del elemento. con la etiqueta `content: 'Esto es un elemento'`
### Modelo de Caja
Contenido: h1, p,.....
Padding: margen interno
Border: Borde del elemento
Margin: Margen externo

#### Unidades de medida
* Relativas
  - Pixeles (px)
  - EM (em) : Relativo al tamanio del contenedor padre o del mas cercano.
  - REM (rem) :  Relativo al tamanio del body
  - Porcentaje ( % ):  Unidad de medida sumamente flexible, usado para hacer responsivo


* Absolutas
No se deben usar por que no son flexibles

#### Elementos 
* Elementos de bloque : son aquello que ocupan el 100% del espacion donde estan contenidos.
En este caso la propiedad Display viene seteada a block.

`Las propiedades que son configurables para estos elementos son: width, height, padding, border, margin`

Elementos: h1, p,




* Elementos de linea: Son aquellos que ocupan solo el espacio del elemento
En este caso la propiedad Display viene seteada a inline.
elementos: a

#### Propiedades

  - Relativa
  - Estatica
  - Absoluta
  - Fija
  - Flotant

* DISPLAY: Propiedad para especificar si un elemento es de linea o de bloque.
  - block: elemento bloque
  - inline: elemento de linea
  - inline-block: para que se ajusten a lado del otro y aun asi podamos usar las propiedades en block.

 * FLOAT:  Propiedad para hacer flotar a un componente con respecto al elemento padre.
  - right: Manda a flotar a lado derecho del elemento padre
  - left: Manda a flotar a lado izquierdo del elemento padre
  `Debido a que el height del elemento padre es igual a la altura maxima de sus hijos y estos pueden estar flotando puedes correjir mediante un div adicional y seteandole en css la propiedad clear:both`
* POSITION: 

  - relative: podemos mover la caja a coordenas con las siguientes propiedades
    + lef : Empujamos desde la izquierda hacia la derecha
    + top: Se mueve 20 px hacia abajo
    + right: Empujamo desde la derecha hacia la izquierda
    + button: Empujamoshacia arriba

  - absolute: Apila los elementos con posicion absolute obviando los objetos pocicionado con pocion relativa.

  - fixed: Da una pocicion fija al elemento.

  * BOX-SIZING: 
    - content-box: Valor por defecto que al momento de generar un padding el tamanio de la caja se incrementa

    - `border box: El padding se agrega de forma interna sin afectar el tamanio de la caja` 


### FlexBox
  Conjunta de propiedades que nos permiten distribuir de una manera mas flexible

**Caja Padre**
_______________________
  * DISPLAY 
    - flex : Vuelve a todos los elementos hijos sean flexibles

      `display:flex;`

    * **flex-direction:**
      + row : (default), en fila desde la izquierda
      + row-reverse : fila en sentido inverso desde la derecho
      + column : en columna desde arriba 
      + column-reverse : en columna desde abajo
    * **flex-wrap:**
      + nowrap : (default) cambia el tamanio de las cajas para acomodarlas en una sola linea
      + wrap : Cuando no exista mas espacion ubica en una nueva linea las demas cajas
    * **`flex-flow`**
      Propiedad que incluye flex-direction y flex-wrap
      
      Ejm. `flex-flow: row wrap`

    * **justify-content** : Desplazamiento horizontal
      - flex-start : (default)
      - flex-end
      - center
      - space-between
      - space-around
    * **align-items** : Desplazamiento vertical
      - flex-start : Coloca arriba
      - flex-end : Coloca abajo
      - center : coloca en el centro
      - strech : Calcula el 100% de altura, `siempre y cuando no exista height en la caja hija`.
      - baseline : alinea los textos en las cajas con las otras cajas

    * **align-content** Desplazamiento vertical, `solo funciona cuando hay mas de una linea`
      - center : centra
      - flex-start : coloca al inicio
      - flex-end : coloca al final
      - strech : (Default) coloca llenando el 100% de su espacio. `Para funcionar no debe poner un height a la caja hija`
      - space-betwen : coloca una fila arriba la otra abajo y si hay otra en la mitad
      - space-aroud :  Deja un espacio entre arriva y abajo y luego los coloca en el mismo espacio entre las cajas hijas
**Caja Hija**
_______________________

    * order : Define un orden
    * flex-grow : 'ignora el max-width' y de fine el porcentaje de crecimiento. 
    * flex-shrink: El porcentaje de reduccion funciona si el padre `flex-wrap: nowrap;`. 
    * flex-basis: es equivalente a widht
    * flex: resumir las propiedades anteriores
       Ejm. `flex: 1 1 200px`
    * align-self: Desplazamiento vertical
      - flex-start : Coloca arriba
      - flex-end : Coloca abajo
      - center : coloca en el centro
      - strech : Calcula el 100% de altura, `siempre y cuando no exista height en la caja hija`.
      - baseline : alinea los textos en las cajas con las otras cajas
### Disenio Adaptativo
1. Viewport
`<meta name='viewport' content='width-device-width, initial-scale=1.0, user-scalable-no, maximum-scale=1.0, minimum-scale=1.0,'/>`

2. Imagenes y videos responsivos
  * width : en porcentaje
  * max-width: crecimiento maximo en pixeles

2. Definir Media Querys
  Puede aplicar estilos para cada tipo de pantalla
  * print : Vista de impresion
  * min-width : Tamanio minimo horizontal
  * max-width : Tamanimo maximo horizontal
  * min-height : Tamanio minimo vertical
  * max-height : Tamanio maximo vertical
  * orientation: Pocicion en la que se encuentra el dispositivo.
  * resolution: Tamanio ocupado por el browser en pixeles
  * color : Detecta si la pantalla en que visualiza el sitio
  * light-level: Densidad de luz del dispositivo
    ```
    //@ media (print/screen/ all) 
    @media print
    {
      img{
        width: 100%;
      }
      h1{
        color: red;
        text-align: center;
      }
    }

    @media all and (min-width: 421px) ans (max-width:780px){
      img{
        wdth:80%
      }
    }
    ```
### Patrones de Disenio
* Tiny Tweak: Sitios demasiados simples se plantes que se disenie en una sola columna.
* Mostly Fluit: Se basa en despositivos pequenios se apila todo en una sola columna
  Ejm:
  ```
    *{
        box-sizing: border-box;
    }
    body{
        background-color: #858585;


    }
    .contenedor{
        background-color:white;
        width: 100%;
        max-width: 800px;
        display: flex;
        flex-wrap: wrap;
        margin: auto;
        padding: 20px;
    }
    .caja1{
        width: 100%;
        background-color: green;
        height: 300px;
    }
    .caja2{
        width: 50%;
        background-color: aqua;
        height: 200px;
    }
    .caja3{
        width: 50%;
        background-color: blue;
        height: 200px;
    }
    @media all and (max-width: 420px) {
        .caja2, .caja3{
            width: 100%;
    }
  ```
 * Column Drop: SImilar a Mostly fluit pero toma en cuenta la importancia para apilar los elementos
 ```
  *{
      box-sizing: border-box;
  }
  body{
      background-color: #858585;


  }
  .contenedor{
      background-color:white;
      width: 100%;
      max-width: 800px;
      display: flex;
      flex-wrap: wrap;
      margin: auto;
      padding: 20px;
      font-size: 20px;
      font-weight: bold;
  }
  .caja1{
      width: 20%;
      background-color: green;
      height: 500px;
  }
  .caja2{
      width: 60%;
      background-color: aqua;
      height: 500px;
  }
  .caja3{
      width: 20%;
      background-color: blue;
      height: 500px;
  }
  @media all and (min-width: 421px) and (max-width: 760px) {
      .caja1{
          width: 30%;
      }
      .caja2{
          width: 70%;
      }
      .caja3{
          width: 100%;
      }
  }
  @media all and (max-width: 420px) {
      .caja1, .caja2, .caja3{
          width: 100%;
      }
      .caja1{
          order: 2;
      }
      .caja2{
          order: 1;
      }
      .caja3{
          order:3;
      }
  }
 ```

 * Layout Shifter: Es el mas complejo, tiene muchos breackpoints

 * off-canvas: Patron mayormente usado en celulares...

### Transformaciones
Efectos que permiten modificar pocision forma o tamanio

  * Transform
    - rotate( deg ) : Rota una caja
    - scale( x, y) : Modifica el tamanio de una caja en base a x - y
    - translate (x, y): Traslada de pocicion a una caja. 
      Tambien se puede usar translateX - translateY. `No es para pocicionamiento de objetos en la web, se usa para animaciones`
    - skew( deg, deg ) : Deforma la forma dado valores x y

### Transiciones:
  * transition
    - propiedad_css/all segundos velocidad_trancision;
      + velocidada de trancision
        +ease: Inicie lento y en la mita mas rapito y despues lento
        + ease-in: Empienza lento y luego toma velocidad normal
        + ease-out: Empieza a velocidad normal y despues reduce su velocidad.
        + easy-in-out: Empieze lento luego normal y termina lento
        + linear: Con velocidad constante.
  * transition-delay:
    - segundos para activarse;
### Animaciones
**Declaracion**

  * @keyframes nombre_animacion
    -  [from{}]
      + Propiedades css
    - [to{}]
      + Propiedades css
    - [%{}]
      + Propiedades css
  
  **Invocacion**
  * animation-name:
    - nombre_animacion
  * animation-duration
    - segundos
  * animation-iteration-count:
    - infitive: ejecuta la animacion de forma infinita
  * animation-delay:
    - segundos
### Filtro de imagenes
  * filter:
    + blur(px): para desenfocar
    + grayscale(100%): para escala de filtros
    + drop-shadow( x y blur color): para sombras
      - x en px
      - y en px
      - blur
      - color
    + sepia(%): Efecto sepia
    + brightness(%): Para ajustar brillo
    + contrast() Ajustar el contraste
    + hue-rotate(): Incrementa el valor de los colores
    + invert(100%): Invierte la imagen
    + saturate() Ajustar la saturacion
    + opacity(%): Ajusta la opacidad
# SASS
## Buenas Practicas
* Ubicamos variables globales en un solo archivo


## Variables
```
$variable: 5em;
/*Arreglo*/
$list: 1px solid red;
p{
  order: $variable/2;
  border: list;
}
```
*!default:* Sirve para tomar el valor de la variable ya declarada
```
$main-color: #ffc768;

html {
    $main-color: #AD9161 !default;
    background: $main-color;
}

```
*!global:* Sobreescribe una variable locas 
```
$main-color: #ffc768;

html {
    $main-color: #AD9161 !global;
    background: $main-color;
}
div{
  background: $main-color;
}

```
## @at-root
Es util para saltar el anidamiento en css, y compilarlo por fuera. Sirve para crear componentes independientes.
```

html {
    $main-color: #AD9161 !default;
    background: $main-color;
    @at-root div{
      background: $main-color;
    }
}

```
## Tipos de Datos
* Numeros
* String
* Colores
* Null
* List
  * Declaracion
    $lista: hola mundo, que tal;
  * Tomar el valor de una lista
    nth($lista, 1) 
* Maps
  * Declaracion
    ```
    $map: (
      clave1: valor1,
      clave2: valor2
    )
    ```
  * Tomar el valor de un map
     map-get($map, clave1)
  * Iterar un map
    ```
    .social-button{
      @each $clave $valor 
        in $map {
          &.#{$clave} {
            background-color: $color;
          }
        }
     }
    ```
## Operaciones
* Adicion o concatenacion ( + )
* Resta ( - )
* Division ( / ): `Usar interpolacion (#{$val1} / #{val2}) si lo que se requiere es enviar el caracter / en lugar de la division`
* Multiplicacion ( * )
* Modulo ( % )
* Comparacion ( >, <, >=, <=, ==, != )
* Operadores Logicos ( or , and )

## @import "styles.scss";
Util para importar archivos
## extend .bloque
Extiende todas las caracteristicas de un bloque de codigo cerado

## PlaceHolder
```
%placeholder{
  width: 200px;
  height: 200 px;
}
.banner {
 @extend %placeholder;
}
```
## Mixin
```
@mixin primer-mixing($line-height, $font-size, $display: inline-block){
  display: $display;
  line-height: $line-height;
  font-size: $font-size;
  padding: 0 1em;
}
.button {
  @include primer-mixing(3, 1em, inline-block)
  &.small {
    @include primer-mixing(2.5, 0.8em,inline-block)
  }
  &.medium {
    @include primer-mixing(2.5, 0.8em)
  }
  &.very-small {
    @include primer-mixing($line-height: 2.5, font-size: 0.8em)
  }
}
```
`Los argumentos por defecto es recomendable dejarlos al ultimo de los argumentos para que en el momento de incluirles no se envie el argumento`

`Para incluir mixins muy grandes es recomendable enviar argumentos especificado el nombre de los argumentos`
###Mixin con multiples argumentos
```
@mixin multiple($box-shadow...){
  box-shadow: $box-shadow;
}
.box {
  @include multiple(1px solid red, 2 solid blue, 5px solid white, 10px solid green);
}

```
### Media Queries con Mixin

```
@mixin mq($min-width){
  @media screen and (min-width: $min-width) {
    //codigo
    @content;
  }
}

.box {
  color: red;
  @include mq(40em){
    color: green;
  }
   @include mq(60em){
    color: purple;
  }
}

```
### Proporciones
```
@mixing radio( $width, $height ) {
  height: 0;
  overflow: hidden;
  padding-bottom: percentage($h / $w);
  width: 100%
  background: red;
}
.radio {
  @include radio ( 16, 9 )
}
.radio {
  @include radio ( 16, 9 );
  position: relative;
  iframe,
  video,
  object {
    position: absolute;
    width: 100%;
    height: 100%;
  }
}
```

## Funciones
Devuelven tipos de datos no bloques
**FUNCIONES CSS**
* rgb: rgba(255, 0, 255  ) 
* calc(): calc(100% - 20%)
* scale(): transform: scale(1.2)
* rotate()
* translate(x, y)
* linear-gradient()  repeting-linear-gradient() 
* radial-gradient() repeting-radial-gradient()
* attr()

**FUNCIONES SASS**
* unquote(): elimina comillas a un string
* quote(): ande comillas al string
* percentage(): convierete un numero a porcentaje
* round(): redondea un numero decimal
* nth($list, $index): obtener un valor de un listado
* map-get($map, $key): obtener un valor de un map especificando su clave
* type-of(): Obtiene el tipo de una variable
* unit() devuelve la unidad de un numero
* unitless() devuelve un boolean, true si no tiene unidad y false si tiene unidad.
**FUNCIONES AVANZADAS SASS**
1. Instropeccion: preguntarse a si mismo
* type-of
* unit()
* unitless()
* inspect(): ver un valor
* varianle-exist(variable)
* function-exist(function)
* mixin-exists(mixinName)
* call(funcion, argumentos)

2. Funciones para strings
* quote()
* unquote()
* str-lenght($string)
* str-index($string, 'subcadema')
* str-insert($string, 'subcadena', $index)
* str-slice($string, $inicio, $final)
* to-upper-case()
* to-lower-case()

3. Funciones numericas
* round(): Redonde dinamico
* percentage()
* floor($numero): Redondear hacia bajo
* ceil($numero): Redondear hacia arriba
* max(1,3,4,5): No reciben listas como parametros
* min(1,2,3,4,5)
* abs($numero): Valor absoluto
* random([$numero])

4. Funciones de listas
* nth($list, $index)
* lenght($list)
* join($list1, $list2, $list3, [$separador]) el separador puede omitirse o o puede tomar los valores (space/comma)
* append($list, $value, [separador]) Aniade un nuevo elemento
* zip($list1, $list2): Crea una lista multidimensional con las listas pasadas como argumentos


5.  

### Crear funciones
```
// FUNCION PARA SUMAR
@function suma( $a, $b: 10 ) {
  @return $a +@b;
}
.suma {
  width: suma(10em, 2)
}

// FUNCION PARA PARSEAR PX A EM
@function parseEM( $element, $father ) {
  @return ( $element / $father) * 1em;
}
div{
  $fz: 24px;
  font-size: $fz;
  p {
    font-size: em(7px, $fz);
  }
}

// IMAGE PATH
$path: '../assets/img/';
@function imagePath( $img ){
  @return url($path + $img)
}
div {
  background: img('bg.jpg')
}


```
