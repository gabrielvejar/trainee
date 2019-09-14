<h2 id="primera-etapa-4-semanas-">Primera etapa (4 semanas)</h2>
<table>
    <thead>
        <tr>
            <th>Objetivos</th>
            <th>Descripción</th>
            <th>Duración</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Formulario de votación (1° parte)</td>
            <td>Se construye el <a href="http://192.168.1.33/git/ART/TrainingDesarrollo/wiki/_blob/prueba%20desarrollador%20facil.pdf">formulario
                    de votación</a> con el esquema de tres archivos (index, command, controlador) y sin usar
                librerías
                externas. Separar la lógica en tres archivos mejora el orden y ayuda a comprender el rol de cada
                uno de
                ellos dentro de la aplicación. El formulario debe cumplir con todas las validaciones indicadas,
                tanto
                en Javascript como en php.</td>
            <td>4 días</td>
        </tr>
        <tr>
            <td>Totalizado de votos (2° parte)</td>
            <td>Se construye sección donde se pueda observar el totalizado de votos. En los archivos se debe
                separar la
                conexión y las funciones genéricas, esto da un acercamiento al uso y creación de componentes que ya
                se
                están implementando en los sistemas de facturación Desis. Se cambian las consultas de pg_query a
                pg_query_params que es la forma mas parecida a la que hay en los sistemas</td>
            <td>3 días</td>
        </tr>
        <tr>
            <td>Listado de votos (3° parte)</td>
            <td>Se construye un listado de todos los votos realizados, incluyendo la descarga de los datos en
                formato
                xml y la funcionalidad de eliminar. Se explica de forma general como crear vistas y funciones. Se
                reemplazan consultas, insert, update y delete que se puedan estar haciendo desde php para que se
                hagan
                por medio de funciones de base de datos</td>
            <td>2 dias</td>
        </tr>
        <tr>
            <td>Estándares Base de datos, practica funciones y vistas</td>
            <td>Se explican los estándares, nomenclaturas y buenas practicas en la construcción de funciones y
                vistas de base de datos.

                Ejercicios:
                <ol>
                    <li>Crear vista que muestre en donde, cuando y por quien votaron los candidatos, ya sea por
                        ellos mismos, por otros candidatos o si aun no han votado.
                        La vista debe devolver las siguientes columnas:
                        <ol>
                            <li>votante: candidato que voto</li>
                            <li>candidato: candidato por el que votó, en caso de no haber votado debe decir "--NO
                                HA VOTADO--"</li>
                            <li>region: region donde votó, en caso de no haber votado debe decir "--NO HA VOTADO--"</li>
                            <li>comuna: comuna donde votó, en caso de no haber votado debe decir "--NO HA VOTADO--"</li>
                            <li>fechahora: La fecha y la hora en que votó, en caso de no haber votado debe decir
                                "--NO HA VOTADO--"</li>
                            <li>voto: booelano que será true cuando haya votado y falso de lo contrario</li>
                        </ol>
                    </li>
                    <li>
                        Crear funcion que al ejecutarla cambie el nombre y la fecha de todos los votantes. Con la
                        restriccion de que los nombres sean unicos y no puede haber dos votos un mismo dia.
                    </li>
                </ol>
            </td>
            <td>3 días</td>
        </tr>
        <tr>
            <td>Flujo de producción de software Desis y practica base de datos dblink y type</td>
            <td>Explicacion del uso de dblink y type. Como crearlos, como y cuando usarlos.

                Ejercicio:
                Crear función para migrar datos de los votantes de otro trainee (origen) a su propia base de datos
                (destino), para
                ello esta función:
                <ul>
                    <li>Correrá en una base de datos que pueda se pueda hacer dblink (sysunico7) a la cual los
                        trainee no tendran acceso. Estos entregarán script final al encargado del trainee para
                        correrlo</li>
                    <li>Creará un type con los campos necesarios de la tabla de origen</li>
                    <li>Recorrerá los datos de los votos de la tabla de origen a través de un dblink en una
                        instruccion for volcando los datos en una variable del tipo que fue creado previamente
                        (parecido a hacerlo a un tipo RECORD)</li>
                    <li>Por cada iteracion del for deberá hacer un dblink llamando a la funcion de insercion de
                        votos que esté en la base de datos de destino <em>por ejemplo: fn_voto_i(...)</em>
                        mandandole como parametros los datos de la base de datos de origen</li>
                    <li>La funcion debera devolver la cantidad de registros ingresados en la base de datos de
                        destino</li>
                </ul>
            </td>
            <td>2 dias</td>
        </tr>
        <tr>
            <td>Prueba completa evaluación</td>
            <td>Se realiza la prueba completa. Para poder medir los avances de los programadores</td>
            <td>1 día</td>
        </tr>
        <tr>
            <td>Corrección de las evaluaciones</td>
            <td>Se entrega feedback acerca de la evaluación y se realizan las correcciones de ser necesario</td>
            <td>5 días</td>
        </tr>
    </tbody>
</table>
<h2 id="segunda-etapa-4-semanas-">Segunda etapa (4 semanas)</h2>
<table>
    <thead>
        <tr>
            <th>Objetivos</th>
            <th>Descripción</th>
            <th>Duración</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Entregas. Work Space</td>
            <td>Se explica cual es el formato y como deben ser las entregas de los requerimientos asignados. Así
                también el buen uso de los espacios de trabajo en los distintos proyectos</td>
            <td>1 día</td>
        </tr>
        <tr>
            <td>La senda del Desarrollador</td>
            <td>Se explica de forma detallada el proceso de desarrollo de un requerimiento de mantención, desde el
                entendimiento del requerimiento hasta la ubicación y reparación de precisa de lo solicitado.
                Después de la explicación se asignará un requerimiento que deberá desarrollar en paralelo al
                aprendizaje de los componentes que proceden <b>Nota: En ambiente de prueba training (sysunico7)</b>,
                de tal forma que cuando haya terminado la sección de los componentes entregue este requerimiento
                aplicando lo aprendido</td>
            <td>1 día</td>
        </tr>
        <tr>
            <td>Estándares técnicos</td>
            <td>Se definen cuales son las reglas y convenios de la empresa con respecto a codificación. Modularización y depuración de  código</td>
            <td>2 días</td>
        </tr>
        <tr>
            <td>Estándares Funcionales</td>
            <td>Se definen cuales son las reglas y estándares de las funcionalidades que deben cumplir las
                aplicaciones
                del sistema</td>
            <td>2 días</td>
        </tr>
        <tr>
            <td>Componente DataBase</td>
            <td>Se explora y se explica en profundidad el componente. Mientras se realizan ejemplos practicos de
                este</td>
            <td>2 días</td>
        </tr>
        <tr>
            <td>Componente Base de datos</td>
            <td>Clase para trabajar con postgreSQL desde php <br>
           Ejercicio: Realizar un consulta buscando el último registro en la tabla public.usuario duplicarlo cambiando su usuario al que el trainee tenga. Para ello deberá usar $Base->query_params </td>
            <td>1 días</td>
        </tr>
        <tr>
            <td>Componente MessageBox</td>
            <td>Se construye pantalla que con 6 botones, que levanten cada uno de los tipos de messagebox descritos
                en
                la documentación y además uno &quot;libre&quot;, donde debe utilizar lo aprendido, ya sea
                combinando o
                personalizando el messagebox.</td>
            <td>2 dia</td>
        </tr>
        <tr>
            <td>Componente LightBox</td>
            <td>Se construye pantalla que con 4 botones, Crear cuatro botones y que cada boton levante un lightbox
                distinto, es decir : <em> Un botón que levante un lightbox con la función &quot;ShowInfo&quot; del
                    componente. </em> Un botón que levante un lightbox con la función &quot;ShowInfoDentro&quot;
                del
                componente. <em> Un botón que levante un lightbox con la función &quot;ShowInfoWidget&quot; del
                    componente. </em> Y por último un botón que levante un lightbox y realice una acción
                &quot;creativa&quot; a elección propia. NOTA: Experimentar con los atributos, métodos y funciones
                del
                componente.</td>
            <td>2 dia</td>
        </tr>
        <tr>
            <td>JasperReports</td>
            <td>Creación de reportes Jasper con iReport</td>
            <td>1 día</td>
        </tr>
        <tr>
            <td>TDESIS (Tesis Desis)</td>
            <td>Se construye una aplicación, ya sea un CRUD o algún tipo de funcionalidad, que requiera la
                implementación de los componentes antes aprendidos. Y esta pueda ser usada para mejorar los
                procesos
                del training y/o del desarrollo en general.</td>
            <td>5 días</td>
        </tr>
        <tr>
            <td>Búsqueda de archivos. util.js, validadores, etc.</td>
            <td>Se explica las formas mas comunes de ubicar archivos entre los directorios. Se explica de que
                consiste
                el util.js, validadores y demás funciones genéricas de la empresa</td>
            <td>1 días</td>
        </tr>
    </tbody>
</table>
<h2 id="tercera-etapa-4-semanas-">Tercera etapa (4 semanas)</h2>
<table>
    <thead>
        <tr>
            <th>Objetivos</th>
            <th>Descripción</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td> Prepractica </td>
            <td colspan="2">Consiste en la realización de 2 requerimientos, con el fin de que el participante se enfrente a un
                escenario mas real del desarrollo y aplicando los conocimientos obtenidos en el Training.</td>
        </tr>
        <tr>
            <td>Practica</td>
            <td colspan="2">El candidato deberá desarrollar de 3 a 5 requerimientos con duraciones cortas, asignados y
                supervisados por el encargado del Training. Esta etapa finalizará una vez que los requerimientos
                asignados lleguen a estado de QA, se deberá dar cierta prioridad a estos requerimientos, para que
                sean revisados y avanzados lo antes posible.</td>
        </tr>
    </tbody>
</table>
