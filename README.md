
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

# Vista

La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

Las vistas, como su nombre nos hace entender, contienen el código de nuestra aplicación que va a producir la visualización de las interfaces de usuario, o sea, el código que nos permitirá renderizar los estados de nuestra aplicación en HTML. En las vistas nada más tenemos los códigos HTML y PHP que nos permite mostrar la salida.

En la vista generalmente trabajamos con los datos, sin embargo, no se realiza un acceso directo a éstos. Las vistas requerirán los datos a los modelos y ellas se generará la salida, tal como nuestra aplicación requiera.


## Imagen Vista

![App Screenshot](https://codigosdeprogramacion.com/cursos/wp-content/uploads/2017/06/MVC.jpg)

# Controlador

El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

### Responsable de:

- Recibe los eventos de entrada (un clic, un cambio en un campo de texto, etc.).

- Contiene reglas de gestión de eventos, del tipo "SI Evento Z, entonces Acción W". Estas acciones pueden suponer peticiones al modelo o a las vistas. Una de estas peticiones a las vistas puede ser una llamada al método "Actualizar()". Una petición al modelo puede ser "Obtener_tiempo_de_entrega ( nueva_orden_de_venta )". 

## Imagen Controlador

![App Screenshot](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSgNMZYHclYsC-36KggyTxQYuUmsnxyH8ADaQ&usqp=CAU)



## Ejemplo Vista

```javascript

//VISTA

<style>
    th{
        width: 8rem;
        text-align: left;
        border-bottom: 1px solid black;
    }
    td{
        width: 8rem;
    }
</style>

<h1>Ejemplo 5: Listado de coches</h1>
<table>
    <tr>
        <th>Marca</th>
        <th>Modelo</th>
        <th>Color</th>
        <th>Propietario</th>
    </tr>
    <?php foreach ($rowset as $row): ?>

        <tr>
            <td><?php echo $row->marca ?></td>
            <td><?php echo $row->modelo ?></td>
            <td><?php echo $row->color ?></td>
            <d><?php echo $row->propietario ?></td>
        </tr>

     <?php endforeach; ?>
</table>



// Modelo 

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

// Controlador

<?php

class CocheController
{
    var $coches;

    function __construct()
    {
        $this->coches = [
            1 => new Coche("Wolkswagen","Polo","negro","Rebeca"),
            2 => new Coche("Toyota","Corolla","verde","Marcos"),
            3 => new Coche("Skoda","Octavia","gris","Mario"),
            4 => new Coche("Kia","Niro","azul","Jairo")
        ];
    }

    public function index(){

        //Asigno los coches a una variable que estará esperando la vista
        $rowset = $this->coches;


        //Le paso los datos a la vista
        require("view/index.php");

    }

}
