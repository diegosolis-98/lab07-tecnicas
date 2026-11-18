# Tarea: Mi prompt avanzado 
Herramienta de IA usada: chatGPT.

## Tarea elegida
Se le pidio a la IA realizar un sistema de registro de alumnos y cursos por matrícula.
## Version 1: prompt basico
```text
 Diseña un sistema de registro de alumnos y cursos matriculados en JAVA. Realízalo paso a paso por clase necesaria.
```
Para esta versión básica solo se hizo el pedido de manera general usando la técnica "chain of thought" con el objetivo de hacer el seguimiento del desarrollo.
## Version 2
```text
Diseña un sistema de registro de alumnos y cursos en JAVA. El sistema debe registrar por clase Alumno (código, nombre, ArrayList de clase Curso cursos), la clase Curso (código, descripción y créditos). 
Ejemplos: - Curso curso1=new Curso("BS101","Bases de datos",3.5 "double rango 1.0 a 5.0").
- Alumno alumno=new Alumno(101 "Int rango 101 a 110,"Martin Pérez") dentro del mismo constructor se inicializa el arrayList.
- alumno.agregaCurso(curso1)--> public void agregaCurso(curso){ cursos.add(curso);}.
Realiza paso a paso a partir de la clase Curso hasta la clase main.
```
Para la versión 2 se uso las técnicas "chain of thought" y "few-shot". Lo que mejoro de la versión anterior es que se redujo la cantidad de código mostrado y complejidad y se acerca mas a lo que buscamos gracias a los ejemplos mostrados de ingreso de datos y al pedido de paso a paso desde la clase Curso para mantener el orden.
## Version 3: prompt final
```text
Se desea diseñar un sistema de registro de alumnos y cursos matriculados por Alumno en Java. En primer lugar paso a paso realiza la clase Curso (código, descripción, créditos).

Ahora realiza la Clase Alumno (código, nombre, ArrayList de Curso) de la misma manera paso a paso considerando método para agregar el curso en el arrayList.

Ahora una vez hecho: Actúa como un profesor de programación, revisa los datos y añade restricciones necesarias al ingresar datos por ejemplo en los créditos generalmente se ingresa como double en un rango de 0.5 a 5.0. Finalmente muestra el código completo reescrito e indica que cambios hiciste.
```
Para la versión final se uso las técnicas "descomposición", "chain of thought" y autocrítica. Mejoro el orden y la claridad secuencial de la resolución del problema al declarar paso a paso por realizar primero una clase y luego otra. Tambien, se añadio restricciones de ingreso de datos para evitar datos nulos o negativos.
## Tecnicas usadas en el prompt final
|Párrafo|Técnica usada|
|-------|-------------|
|1|Descomposición y chain of thought|
|2|Descomposición y chain of thought|
|3|Descomposición y autocrítica|
## Evaluacion del resultado
|Criterios|V1|V2| V3 Final|
|---------|--|--|---------|
|Organización y estructura de clases|No|Sí|Sí|
|Aplicación del encapsulamiento|Sí |Sí |Sí|
|Gestión de cursos matriculados|Sí|Sí|Sí|
|Claridad, modularidad y facilidad de comprensión|No|Sí|Sí|
|Aplicación de restricciones|No|Sí (Parcial)|Sí|
## Por que elegi estas tecnicas
Porque se me hace mas eficiente pedirle a la IA por ejemplos de ejecución de tareas la realización de un pedido, tambien por pasos generar código. Para finalizar por añadir restricciones mediante una autocrítica al pedirle que considere el ingreso de datos no lógicos o no válidos.
