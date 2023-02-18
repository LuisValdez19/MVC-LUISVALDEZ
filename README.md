
# "MODELO (MVC)" 
## Luis Fernando Espinoza Valdez 5A
Modelo Vista Controlador (MVC) es un estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.

Se trata de un modelo muy maduro y que ha demostrado su validez a lo largo de los años en todo tipo de aplicaciones, y sobre multitud de lenguajes y plataformas de desarrollo. 

## MVC

- El Modelo que contiene una representación de los datos que maneja el sistema, su lógica de negocio, y sus mecanismos de persistencia.

- La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

- El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.



## Ejemplo de MODELO

![App Screenshot](https://codigofacilito.com/photo_generales_store/29.jpg)

## Modelo de Representación de Datos

En la capa Modelo encontraremos siempre una representación de los datos del dominio, es decir, aquellas entidades que nos servirán para almacenar información del sistema que estamos desarrollando. Por ejemplo, si estamos desarrollando una aplicación de facturación, en el modelo existirán las clases Factura, Cliente o Proveedor, entre otras.

## Funcionalidades del MODELO

- Separación de las tareas de aplicación (lógica de entrada, lógica de negocios y lógica de interfaz de usuario), capacidad de prueba y desarrollo controlado por pruebas (TDD) de forma predeterminada.

- Un marco extensible y conectable. Los componentes del marco de ASP.NET MVC están diseñados para que se puedan reemplazar o personalizar con facilidad. Puede conectar su propio motor de vista, directiva de enrutamiento de URL, serialización de parámetros de método y acción, y otros componentes.

- Un eficaz componente de asignación de direcciones URL que permite crear aplicaciones que tengan direcciones URL comprensibles y que se puedan buscar.

- Sencillez para crear distintas representaciones de los mismos datos.

- Facilidad para la realización de pruebas unitarias de los componentes, así como de aplicar desarrollo guiado por pruebas (Test Driven Development o TDD).

- Separación clara de dónde tiene que ir cada tipo de lógica, facilitando el mantenimiento y la escalabilidad de nuestra aplicación.


## Ejemplo Modelo 

```javascript
<?php

//MODELO

class Coche
{
    //Variables o atributos
    var $marca;
    var $modelo;
    var $color;
    var $propietario;

    function __construct($miMarca,$miModelo,$miColor,$miPropietario){

        $this->marca = $miMarca;
        $this->modelo = $miModelo;
        $this->color = $miColor;
        $this->propietario = $miPropietario;

    }

    //Funciones o métodos
    function setMarca($miMarca){

        $this->marca = $miMarca;

    }

    function getMarca(){

        return $this->marca;

    }

    function setModelo($miModelo){

        $this->modelo = $miModelo;

    }

    function getModelo(){

        return $this->modelo;

    }

    function setColor($miColor){

        $this->color = $miColor;

    }

    function getColor(){

        return $this->color;

    }

    function setPropietario($miPropietario){

        $this->propietario = $miPropietario;

    }

    function getPropietario(){

        return $this->propietario;

    }
}
