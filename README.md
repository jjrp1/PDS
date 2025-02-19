# PDS

# P2.A.1 - Vigilancia de Exámenes

En la facultad se desea hacer una aplicación para gestionar profesores, asignaturas, exámenes y vigilancias realizadas por cada profesor en cada examen.

Cada asignatura está asociada a una titulación y tiene un profesor responsable.

En cada convocatoria (febrero, junio y julio) se realiza un examen de cada asignatura, cada uno en una fecha determinada. Con suficiente antelación, antes del periodo de exámenes, el secretario de la facultad asigna a cada examen un turno (mañana, tarde), una o varias aulas y el profesor responsable del mismo. Este profesor responsable es el encargado de determinar si es necesario algún profesor más para ayudar a vigilar el examen, y de solicitarlo, en su caso, como mínimo con 15 días de antelación a la celebración del examen.

<p style="text-align: justify;">
El secretario de la facultad recibe una notificación cada vez que se solicitan vigilantes para un examen. El secretario revisa periódicamente estas solicitudes y las valida asignando profesores vigilantes al mismo y avisando a los profesores implicados para que confirmen la vigilancia. Esta revisión de solicitudes se realiza de la siguiente manera: el secretario de la facultad inicia la validación de la solicitud, tras lo cual el sistema asignará las vigilancias solicitadas a los profesores con menos vigilancias hasta el momento y que no tengan un examen en el mismo día y turno. En caso de empate el sistema seleccionará al profesor vigilante de manera aleatoria. El secretario entonces validará esa asignación y el sistema avisará automáticamente a los profesores seleccionados para que verifiquen que pueden realizar la vigilancia y la confirmen o bien indiquen que no les es posible realizar dicha vigilancia.
</p>

![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-a1.puml)

> **NOTAS**: Representamos `turno` como una generalización de `Diurno` y `Tarde` por indicaciones del profesor.

# P2.A.2 - Golf

La Federación Española de Golf tiene mucho trabajo en los últimos años, de manera que ha decidido crear una aplicación que gestione los jugadores, los torneos y los campos federados con las siguientes indicaciones:

- Cada jugador podrá inscribirse en el sistema y registrarse en un torneo determinado. Si el jugador no dispone de caddie propio, el caddie master le asignará uno para jugar en dicho torneo.

- Todos los jugadores tienen una clasificación (junior, sénior, aficionado, profesional, veterano) y un hándicap exacto. Los hándicaps tienen 5 categorías y se determinan según los resultados de los torneos disputados.

- El sistema tiene que ir actualizando el hándicap automáticamente, y para ello en cada torneo el secretario del mismo tiene que registrar el resultado de cada jugador (número de golpes y número de puntos) en el torneo. El hándicap de cada jugador no se actualiza en ese momento, sino que se actualiza automáticamente cada domingo a las 12:00, y se publica en la web de la Federación.


![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-a2.puml)


# P2.B.1 – Centro Penitenciario

Dados los últimos altercados y el alto nivel de población carcelaria, un centro penitenciario
decide desarrollar una aplicación software que permita gestionar a los presos y trabajadores
del mismo.

Cuando un preso nuevo entra en el centro penitenciario se registra en el sistema indicando su
DNI, su nombre, y su historial delictivo. Este historial está formado por las veces que el preso
ha sido condenado por distintos tipos de delitos (desfalco fiscal, robo, homicidio, fuga, etc.)
realizados a lo largo del tiempo. Por cada condena se registra la fecha en que se cometió el
delito, fecha de entrada a la cárcel y la duración total de la condena. Una vez registrado, el
preso automáticamente será asignado a una celda perteneciente a un módulo carcelario
distinto según si ha cometido un delito de sangre o no. Así, un preso que haya cometido un
delito de sangre será asignado al módulo de alta seguridad y si por el contrario sólo ha
cometido delitos menores será asignado al módulo de baja seguridad. Una celda puede
contener como mucho dos presos.

Los trabajadores del centro penitenciario son guardias que trabajan dentro de un módulo y
tienen asignada la vigilancia de 6 a 10 celdas consecutivas. Para evitar que los presos se
familiaricen con los guardias, los trabajadores rotan en las distintas celdas y módulos cada
mes. Esta asignación se realiza de manera aleatoria teniendo en cuenta que un mismo guardia
no puede vigilar la misma celda en un periodo de un año. Además, sólo un guardia es
supervisor de un módulo.

Todos los días por la mañana y por la noche se realizan inspecciones en las celdas por cada
guardia encargado de las mismas, que registrarán la inspección realizada, la fecha y hora que
se ha realizado e indicará si ha habido algún incidente dentro de la misma como puede ser la
detección de droga, armas, etc. Estas incidencias están tipificadas según el código carcelario
internacional. En el caso de producirse una incidencia, el sistema avisará al alcaide quien
tendrá que seleccionar un castigo para los presos de la celda según el incidente detectado.
Una vez al año por Semana Santa se indulta a un preso que saldrá en la procesión del Domingo
de Resurrección. Para ello, el sistema seleccionará un listado de presos candidatos a ser
indultados. Para poder formar parte de ese listado al preso debe quedarle menos de un año de
condena y no se debe haber producido ninguna incidencia en su celda en el último año. De
este listado de presos candidatos el alcaide seleccionará el preso que será indultado ese año.
Por último, un preso podrá solicitar online el cambio de celda debido a desavenencias con su
compañero. En este caso será el supervisor del módulo el encargado de decidir si se aprueba
esa solicitud de cambio de celda o no.

![P2.B.2](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-b2.puml)

![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-b1.puml)


# P2.B.2 – Centro de Salud

Se quiere diseñar parte del sistema de información correspondiente a un centro de servicios médicos. Entre las personas relacionadas con este centro, podemos distinguir entre los pacientes y los trabajadores relacionados con los servicios (doctores, enfermeros, coordinadores, administrativos, etc.). Un trabajador estará acreditado para trabajar en al menos un servicio médico. Se registrará la fecha en la que se acreditó para trabajar en cada servicio. Cada trabajador puede estar asignado a un solo servicio (siempre que tenga la correspondiente acreditación). Cada servicio es identificado por un nombre y registraremos una breve descripción, sus áreas de especialidad médica y el coordinador del servicio.

Los pacientes piden una cita por internet para acudir a los servicios médicos para realizar consultas diagnósticas de problemas de salud o para visitas adicionales para su tratamiento, si así lo determina el doctor que diagnosticó su problema. Cuando un paciente pide la cita se registra la fecha y hora de su visita. Si es para una consulta, se registrará también el doctor que le atenderá. Para cada consulta atendida por un médico, el facultativo registrará el diagnóstico del especialista y los tratamientos posteriores. Cada tratamiento recibe un código secuencial único y el especialista indica su prioridad (baja, normal o alta) junto con una breve descripción.

Si el tratamiento es una medicación, se registrará la dosificación (cada 24 horas, cada 12 horas…), la duración del tratamiento (en días), el compuesto activo y opcionalmente el nombre comercial del medicamento. Posteriormente, si el tratamiento lo requiere, el paciente puede solicitar una o varias visitas adicionales (para un tratamiento concreto). Posteriormente el sistema asigna automáticamente el doctor o enfermero que realizará el tratamiento correspondiente a cada visita. Los doctores están facultados para realizar tratamientos que no impliquen medicación. Los enfermeros no pueden diagnosticar pero si realizar tratamientos. Los pacientes pueden pagar directamente las visitas a través de la plataforma virtual, o bien pertenecer a una compañía asistencial (seguro médico). Para cada paciente se recogerá su nombre (nombre propio y apellidos), NIF, fecha de nacimiento, dirección (calle, ciudad, provincia), teléfonos de contacto, nombre y dirección de la empresa en la que trabajan, tipo de servicios que puede solicitar y forma de pago. Para las compañías asistenciales se recogerá su NIF, nombre y dirección (calle, ciudad, provincia, código postal), y teléfono. Cada final de mes el sistema generará las facturas que se remitirán a las compañías asistenciales. 

![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-b2.puml)


# Ejemplo
![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/sample.puml)
