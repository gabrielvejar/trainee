Plan de estudio:
1 Estándares
    a) Estándares Técnicos
    b) Estándares Funcionales
    c) Nomenclatura Base de Datos

2 Estructura
    a) Command, controlador, index
    b) Encapsulamiento de código

3 Framework de la Empresa
    a) Messagebox
    b) Base (query_params: consultas a base de datos)
    c) RS (comunicación javascript a PHP)
    d) util.js, validadores, etc
    e) Grillas

4 Base de Datos
    a) Funciones
    b) Vistas
    c) Dblink
    d) Types
    e) Casting Variables
    f) JOIN

5 Otros
    a) Entregas
    b) Work Space
    c) Búsqueda de archivos
    d) Debugger


Detalle:


1)Command, controlador, index (¿Como separar el código?):

    • ¿Porque separar el código?
    1. Aspectos Positivos
    2. Aspectos Negativo

    • Command
    1. Que debe contener
    2. switch($cmd)
    3. $query, ultima consulta e información devuelta

    • Controlador
    1. class.php
    2. controlador.js
    3. var BD = new BASE();BD.commandFile = "form/compra/command.php";

    • Index
    1. $POSICION
    2. agregar conexion.php
    3. agregar formHeader.php
    4. formFoot.php

2) Base (query_params) (¿Como comunicarse con las BBDD desde PHP?) :

    • Como armar una consulta a Base de datos.
        1. Consultas sin parametros
        2. Consultas con parametros conctenados
        3. Como y cuando pasar parametros por el array 'params'.
           
    • Manejo de datos devueltos 
            1. to_object
            2. query
            3. num_rows
            4. result_error
      
3) RS (comunicación javascript a PHP) (¿Como comunicarse desde JS a PHP?): 

    • Comunicación de JS a PHP.
            1. BD.send
            2. Parametros
               
    • Como obtener información de Base de datos desde JS.
            1. RS.error
            2. RS.numrows
            3. BD.getField

4)Estándares Técnicos (¿En qué se fijará el revisor técnico?):

    • Buenas practicas.
    1. No repertir código
    2. Controlar excepciones y errores

    • Reglas Desis.
    1. Todos los alert en MessageBox
    2. Revisar funciones y recursos de BBDD (deben estar en otros ambiente)
    3. validadores, util.js
    4. Escapar variables al recibirlas por post o get.
       
    • css: img, styles, .css, tags, etc.
    1. img (alt, src, title) 
    2. styles (;)
    3. archivo css

    • Indentación de código.
    1. Como identar el código

    • Motivos de devolución.
    1. Falta de archivos
    2. Error en el nombre de archivos
    3. Error en la ruta del archivo (ambiente, IP, etc)
    4. No corre el archivo .sql o tiene errores
    5. Código basura comentado

5)Encapsulamiento de código (¿Cuando encapsular nuestro código?): 

    • ¿Porque encapsular nuestro código?
    • Encapsulamiento por archivos
    • Encapsulamiento a través de objetos.
      
6) Debugger (¿Como debuggear fallas?): 

    • Debugeando PHP
            1. die
            2. var_dump
            3. print_r
            4. echo
            5. exit
               
    • Debugeando JS
            1. debugger;
            2. Event Listener Breakpoints (google Chrome)
            3. console.log, console.table
            4. Borrador Mozilla Firefox
               
    • Debugeando CSS
            1. Inspeccionador de elementos
            2. Estilos
            3. Jerarquía

7)Estándares Funcionales (¿En qué se fijará el revisor funcional?):

    • Casos de prueba
    1. Como revisar nuestros requerimiento
    2. Cuales serán los casos que realizará el funcional

    • Caracteres especiales (ñaÑAáéíóú ÁÉÍÓÚ 1234567890 !"#$%&/()=¿?¡_-´+{}")
    1. Prueba de entradas con caracteres especiales

    • Flujo completo
    1. Limite de nuestro requerimiento en un flujo completo
    2. Cuando el flujo completo es necesario

    • ¿Cuando corregir errores dentro del requerimiento o generar requerimiento de FALLA?
    1. Errores del sistema, ¿cuando solucionarlo? (criterio vs tiempo)
    2. En caso de Falla que hacer

    • Motivos de devolución.
            1. Títulos incorrectos
            2. Mensajes al usuario
            3. Importancia de MessageBox
            4. Funcionalidad no esperadas
      
8)Nomenclatura Base de Datos (¿Qué detalles debemos cuidar con las Bases de Datos?):

    • Nombrar correctamente funciones, types y vistas.
            1. Nomenclatura
               
    • Nombrar correctamente las variables.
            1. Parámetros de entrada
            2. Variables locales
               
    • Buenas practicas (controlar excepciones, etc).
            1. indices
            2. excepciones
            3. primary key
            4. foreign key
               
    • Motivos de devolución.
            1. nombres
            2. comentarios basura
            3. variables que no se usen


9) Funciones (¿Como trabajar con funciones?): 

    • Armado de funciones
    1. Alias a variables de ingreso
    2. Variables internas
       
    • Returns
    1. Retornando diferentes tipos de datos (varchar, integer, etc)
    2. Retornando vacio (void)
       
    • Record
    1. Usando record
    2. Retornando un record (no muy usado)

    • Usos útiles (trata de datos)
    1. Usando funciones para realizar acciones especiales (con borrado de la fn)

10) Vistas (¿Como trabajar con vistas?):

    • Armado de vistas
            1. crear y modificar vistas
            2. subconsultas
    • Cuando y porque utilizar.
            1. Ejemplos de situaciones donde es recomendable usar vistas


11) Dblink (Conectandonos con otras BBDD):

    • Para que sirven las consultas Dblink.
            1. Ejemplos
    • Armado de consulta Dblink.
            1. Conexión con otras base de datos
            2. Conexión base de datos de configuración

12) Types (¿Cuando usar un Type?):

    • Construcción de types. 
    1. Nomenclatura del tipo Type
    2. Creación de Type

    • Uso de types.
    1. Usando type para retornar datos

13) Casting Variables (¿Como realizar correctamente un Casting, para nuestro objetivo?):


    • Que es hacer un Casting.
    1. Que es y nomenclatura de un Casting

    • Cuando nos sirve realizar un Casting.
    1. Casos necesarios

    • Porque usarlo. 
    1. Motivo de uso

    • Usos útiles (para ahorrar tiempo, pruebas, etc). 
    1. Problemas que se pueden presentar al realizar el generar sql
    2. Como ahorrar tiempo, castiando variables.

      
14) Sentencias SQL (¿Para que sirve las sentencias  y sus usos?): 

	Cuando usar y ejemplos.
    • INNER JOIN   
    • RIGHT JOIN  
    • LEFT JOIN  
    • UNION  
    • DISTINCT  

15) Entregas (Forma correcta de realizar una entrega): 

    • Linea de producción de software.  
    1. Flujo de los requerimiento
    2. Diferencias de ambientes.

    • Requerimientos por falla  
    1. Que desarrollar y que no.
    2. Diferencia con los requerimientos generales 

    • Reglas del archivo SQL.  
        1. Debe correr, sin errores
        2. Sin código comentado

    • Reglas del archivo Ajustes.  
    1. Comentarios
    2. Orden y armado

16) Work Space (¿Como funciona nuestro espacio de trabajo?): 

    • Importancia  
    1. Porque utilizamos un work Space

    • Codificación  
    1. Diferencias entre ambientes de codificación 

    • Modificación (de ser necesario)  
    1. Cambiando la codificación y ruta del Work Space
      
17) Búsqueda de archivos (¿Como buscar un archivo u elemento en nuestro sistema?): 
    • Buscando un archivo simple  
            1. URL navegador
    • Buscando un archivo en un frame  
            1. Abrir marco en navegador
    • Buscando un archivo redirigido.  
            1. Búsqueda en archivos

19) util.js, validadores, etc. (¿Necesitamos algo que todos usan?): 
    • Cuando incluir funciones en estos archivos. 
            1. Criterios para incluir alguna funciones en estos archivos
    • Motivos de devolución. 
            1. Ejemplos posibles devoluciones por no usar las funciones del util.js o validadores

18) Messagebox (¿Como armar un Messagebox?): 
    • Messagebox según ambiente. 
    1. Diferencias entre ambientes
    2. Messagebox y uso con lightbox
       
    • Botones 
    1. Tipo de botones y cuando usarlos

    • Reglas para títulos y mensajes 
    1. Como armar un titulo
    2. Como armar mensajes a usuarios

    • Problemas a presentarse (trabajando con frame u otros). 
    1. Messagebox afuera del frame
    2. Revisión de botones y acciones dentro del frame

20) Grillas (¿Como entender y trabajar con grillas?): 
    • Lógica de grillas.
    1. Como funciona
    2. Revisión de código

    • Armado de grillas.
    1. Filtros
    2. Llenado de datos
    3. Orden de columnas

    • Modificando una grilla.
    1. Como agregar columnas
    2. Como eliminar columnas
    3. Como modificar columnas, filtros, etc

    • Descargar Excel (Botón de grilla).
    1. Armado de exportación a Excel
