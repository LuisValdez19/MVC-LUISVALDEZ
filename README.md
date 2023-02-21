
# "MODELO (MVC)" 
## Luis Fernando Espinoza Valdez 5A
Modelo Vista Controlador (MVC) es un estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.

Se trata de un modelo muy maduro y que ha demostrado su validez a lo largo de los años en todo tipo de aplicaciones, y sobre multitud de lenguajes y plataformas de desarrollo. 

## MVC

- El Modelo que contiene una representación de los datos que maneja el sistema, su lógica de negocio, y sus mecanismos de persistencia.

- La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

- El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

## ¿En que nos ayuda el Modelo Vista Controlador?

El uso de este patrón ayuda a separar las responsabilidades en el desarrollo de una aplicación, lo que facilita la mantenibilidad y escalabilidad del código. Además, permite que varios desarrolladores trabajen en diferentes componentes de la aplicación simultáneamente.

## Benificios del Modelo Vista Controlador

- Separación de responsabilidades: El MVC separa la lógica de negocio, la presentación y el control de eventos en diferentes componentes. Esto facilita la modificación, el mantenimiento y la escalabilidad del código.

- Reutilización de código: La separación de responsabilidades también permite la reutilización de código en diferentes aplicaciones o módulos de la misma aplicación.

- Facilita el trabajo en equipo: El patrón MVC facilita el trabajo en equipo, ya que diferentes desarrolladores pueden trabajar en diferentes partes del código sin interferir con el trabajo de otros desarrolladores.

- Mejora la legibilidad del código: El MVC promueve la escritura de código claro y organizado, lo que facilita su comprensión y modificación.

- Mejora la seguridad: Al separar la lógica de negocio y la presentación, el MVC puede mejorar la seguridad de la aplicación, ya que reduce la exposición de la lógica de negocio a posibles vulnerabilidades de seguridad.

- Facilita las pruebas: La separación de responsabilidades en el MVC permite una mayor facilidad para realizar pruebas unitarias de las diferentes partes de la aplicación.

En general, el patrón de diseño MVC ayuda a mejorar la calidad, escalabilidad, mantenibilidad, seguridad y reutilización del código en aplicaciones de software.

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

## Beneficios de la Vista

- Separación de responsabilidades: La vista se encarga exclusivamente de la presentación de la información al usuario y no tiene conocimiento directo de la lógica de negocio. Esto permite una clara separación de responsabilidades entre la presentación y la lógica de negocio.

- Flexibilidad: La vista puede ser diseñada de diferentes maneras, lo que permite adaptar la aplicación a diferentes dispositivos y necesidades de los usuarios.

- Facilita la mantenibilidad: La separación clara entre la vista y la lógica de negocio facilita la identificación y corrección de errores y la modificación y actualización del código.

- Mejora la legibilidad del código: La vista se encarga exclusivamente de la presentación, lo que permite que el código sea más claro y legible.

- Facilita la accesibilidad: Una vista bien diseñada puede mejorar la accesibilidad para personas con discapacidades visuales o motoras.

- Mejora la usabilidad: La vista puede ser diseñada para mejorar la usabilidad de la aplicación, lo que puede mejorar la experiencia del usuario y aumentar la satisfacción.

En resumen, la vista en el patrón MVC tiene varios beneficios, como la separación de responsabilidades, la flexibilidad, la facilidad de mantenimiento, la legibilidad del código, la accesibilidad y la usabilidad, que contribuyen a mejorar la calidad y la eficiencia del desarrollo de aplicaciones de software.

## Imagen Vista

![App Screenshot](https://codigosdeprogramacion.com/cursos/wp-content/uploads/2017/06/MVC.jpg)

# Controlador

El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

### Responsable de:

- Recibe los eventos de entrada (un clic, un cambio en un campo de texto, etc.).

- Contiene reglas de gestión de eventos, del tipo "SI Evento Z, entonces Acción W". Estas acciones pueden suponer peticiones al modelo o a las vistas. Una de estas peticiones a las vistas puede ser una llamada al método "Actualizar()". Una petición al modelo puede ser "Obtener_tiempo_de_entrega ( nueva_orden_de_venta )". 

## Beneficios del Controlador

- Manejo de eventos: El controlador maneja los eventos generados por la interfaz de usuario y los procesa en consecuencia. Esto permite una separación clara entre la presentación y la lógica de negocio.

- Flexibilidad: El controlador permite una mayor flexibilidad en la forma en que se manejan los eventos y se procesa la lógica de negocio, lo que permite adaptar la aplicación a diferentes situaciones y requisitos.

- Facilita la mantenibilidad: El controlador separa la lógica de negocio de la presentación, lo que facilita la identificación y corrección de errores y la modificación y actualización del código.

- Reutilización de código: El controlador puede ser reutilizado en diferentes aplicaciones o módulos de la misma aplicación, lo que facilita el desarrollo y reduce los costos y tiempos de entrega

- Escalabilidad: El controlador puede ser escalado según sea necesario, lo que permite manejar grandes volúmenes de eventos y datos sin afectar el rendimiento de la aplicación.

En resumen, el controlador en el patrón MVC tiene varios beneficios, como la separación de responsabilidades, la flexibilidad, la facilidad de mantenimiento, la reutilización de código y la escalabilidad, que contribuyen a mejorar la calidad y la eficiencia del desarrollo de aplicaciones de software.

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
