# PDS

# P2.1.a VIGILANCIAS DE EXÁMENES

En la facultad se desea hacer una aplicación para gestionar profesores, asignaturas, exámenes y vigilancias realizadas por cada profesor en cada examen.

Cada asignatura está asociada a una titulación y tiene un profesor responsable.

En cada convocatoria (febrero, junio y julio) se realiza un examen de cada asignatura, cada uno en una fecha determinada. Con suficiente antelación, antes del periodo de exámenes, el secretario de la facultad asigna a cada examen un turno (mañana, tarde), una o varias aulas y el profesor responsable del mismo. Este profesor responsable es el encargado de determinar si es necesario algún profesor más para ayudar a vigilar el examen, y de solicitarlo, en su caso, como mínimo con 15 días de antelación a la celebración del examen.

El secretario de la facultad recibe una notificación cada vez que se solicitan vigilantes para un examen. El secretario revisa periódicamente estas solicitudes y las valida asignando profesores vigilantes al mismo y avisando a los profesores implicados para que confirmen la vigilancia. Esta revisión de solicitudes se realiza de la siguiente manera: el secretario de la facultad inicia la validación de la solicitud, tras lo cual el sistema asignará las vigilancias solicitadas a los profesores con menos vigilancias hasta el momento y que no tengan un examen en el mismo día y turno. En caso de empate el sistema seleccionará al profesor vigilante de manera aleatoria. El secretario entonces validará esa asignación y el sistema avisará automáticamente a los profesores seleccionados para que verifiquen que pueden realizar la vigilancia y la confirmen o bien indiquen que no les es posible realizar dicha vigilancia.

![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-1.puml)

# P2 - Ejercicio 2 (Golf)
![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/p2-a2.puml)


# Ejemplo
![UML-test-ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/jjrp1/PDS/main/sample.puml)
