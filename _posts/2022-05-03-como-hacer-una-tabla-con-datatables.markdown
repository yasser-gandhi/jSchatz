---
layout: post
title: ¿Cómo hacer una tabla con DataTables?
subtitle: Utiliza el plugin de jQuery para realizar una tabla de manera rápida y sencilla
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [jquery, datatables, javascript]
---
[Javascript]: https://developer.mozilla.org/es/docs/Web/JavaScript/
[DataTables]: https://datatables.net/download/
[jQuery]: https://jquery.com/download/
[Bootstrap]: https://getbootstrap.com/docs/5.1/getting-started/download/
[Examples de DataTables]: https://datatables.net/examples/data_sources/dom.html

Uno de las tareas más recurrentes como programador es presentar información contenida de una base de datos en forma de tabla. Si bien, podemos hacerlo de manera nativa con [Javascript][Javascript]{:target="_blank"}, tenemos una alternativa más rápida y sencilla de hacerla. Para ello haremos uso del plugin [DataTables][DataTables]{:target="_blank"}, que es un plugin para la librería [jQuery][jQuery]{:target="_blank"}. 

# Requisitos

- Descargar la librería [jQuery][jQuery]{:target="_blank"} y [Bootstrap][Bootstrap]{:target="_blank"}, ya sea mediante el archivo zip o CDN.

# Procedimiento

- Abre VS Code y crea una carpeta llamada **librerias**. Ve a [jQuery][jQuery]{:target="_blank"} y da click al archivo comprimido. Se abrirá una nueva ventana con código. Selecciónalo todo y copialo.

![]({{"/assets/img/datatables/jquery.png"| relative_url}}){: .mx-auto.d-block :}

- En tu carpeta **librerias**, crea un archivo llamado `jquery.min.js` y pega el código que acabas de copiar.

- Ve a [Bootstrap][Bootstrap]{:target="_blank"} y descarga los archivos **Compiled CSS and JS**. Descomprímelos y busca los archivos `bootstrap.min.css` y `bootstrap.min.js` y arrástralos a la carpeta **librerias**.

![]({{"/assets/img/datatables/bootstrap.png"| relative_url}}){: .mx-auto.d-block :}

- Ahora descarga los archivos `datatables.min.js` y `datatables.min.css` desde [DataTables][DataTables]{:target="_blank"} y agregalos

![]({{"/assets/img/datatables/datatables.png"| relative_url}}){: .mx-auto.d-block :}

- Crea un archivo `index.html` y vincula todos las librerías agregadas: las de extensión **.css** en el head y las **.js** antes de terminar el body. Agrega una hoja extra de CSS y JS para personalizar tus propios estilos y scripts. Se debería ver algo así:


~~~
<head>
    <title>DataTables</title>
    <link rel="stylesheet" href="librerias/bootstrap.min.css">
    <link rel="stylesheet" href="librerias/datatables.min.css">
    <link rel="stylesheet" href="librerias/style.css">
</head>
<body>
    <script src="librerias/jquery.min.js"></script>
    <script src="librerias/bootstrap.min.js"></script>
    <script src="librerias/datatables.min.js"></script>
    <script src="librerias/app.js"></script>
</body>
~~~


- Ahora ve a la sección de [Examples de DataTables][Examples de DataTables]{:target="_blank"} para copiar el siguiente código, tanto de Javascript como HTML.

![]({{"/assets/img/datatables/examples_datatables.png"| relative_url}}){: .mx-auto.d-block :}

### En app.js
~~~
$(document).ready(function() {
    $('#example').DataTable();
} );
~~~

### En index.html (versión mínima)
~~~
<table id="example" class="display" style="width:100%">
        <thead>
            <tr>
                <th>Name</th>
                <th>Position</th>
                <th>Office</th>
                <th>Age</th>
                <th>Start date</th>
                <th>Salary</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Tiger Nixon</td>
                <td>System Architect</td>
                <td>Edinburgh</td>
                <td>61</td>
                <td>2011/04/25</td>
                <td>$320,800</td>
            </tr>
            <tr>
                <td>Garrett Winters</td>
                <td>Accountant</td>
                <td>Tokyo</td>
                <td>63</td>
                <td>2011/07/25</td>
                <td>$170,750</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <th>Name</th>
                <th>Position</th>
                <th>Office</th>
                <th>Age</th>
                <th>Start date</th>
                <th>Salary</th>
            </tr>
        </tfoot>
    </table>
~~~


- Explora el archivo index.html y verás cómo se muestra la tabla con los datos. Además despliega filtros de búsqueda. No obstante, la información nos aparece en inglés. Para traducirlo, ve al apartado de **Plug-ins** y después **Internationalisation**. Allí nos dice cómo utilizar la función. si observas, tendremos que agregar el parámetro `language`. Lo más fácil es copiar el ejemplo y borrar el anterior.

~~~
$(document).ready(function() {
    $('#example').DataTable( {
        language: {
            url: 'dataTables.german.json'
        }
    } );
} );
~~~


- Busca el idioma al que deseas traducir y copia la dirección CDN y sustituyela en la URL de la función.


![]({{"/assets/img/datatables/cdn_traducir_espanhol.png"| relative_url}}){: .mx-auto.d-block :}


- Verás como se traduce automáticamente la tabla. Y listo, ya tienes una tabla hecha mediante el plugin DataTables.

![]({{"/assets/img/datatables/resultado_tabla_traducida.png"| relative_url}}){: .mx-auto.d-block :}


*!Hasta la próxima!*