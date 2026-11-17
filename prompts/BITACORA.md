# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting. Herramienta de IA usada: chatGPT.

##	Ejercicio	2:	Zero-shot, one-shot y few-shot
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5| En tabla con númeracion de comentario, clasificación y justificación.| Si|
| One-shot | 5| Con comentario en comillas, numerado y su clasificación.|Si |
| Few-shot | 5| Solo los comentarios en comillas y su clasificación.| Si|

##	Ejercicio	3:	Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo |318.60 |No | Si|
| Paso a paso | 318.60| Si|Si |

##	Ejercicio	4:	Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|--------------------------------|-----------------------|----------------------|
| A. Sin rol | Sencillo| Si|Publico en general |
| B. Rol docente | Sencillo|Si | Estudiantes|
| C. Rol senior |Técnico|Si |Trabajadores |

##	Ejercicio	5:	Descomposicion
- Paso 1: La IA entrego las funcionalidades que tendra el programa mediante los requisitos propuestos, y mediante esto la propuesta de desarrollo de clases.
- Paso 2: La IA entrego cada clase propuesta en el paso anterior con sus atributos y tipos de dato que almacenará, asi como las responsabilidades de cada clase.
- Paso 3: La IA entrego el código en JAVA del desarrollo de las clases, y también un ejemplo de uso del mismo.
- Paso 4: La IA propuso agregar excepciones o restricciones del ingreso de datos.
- Diferencia con el pedido de 1 sola vez: La diferencia es que el pedido de 1 sola vez entrego una explicación breve del sistema y sus funcionalidades, resultando en el desarrollo de un código extenso con un menú de uso al ejecutar.
##	Ejercicio	6:	Prompt estructurado y autocritica
|Qué revisar|Cumple (Sí/No)|
|-----------|--------------|
|¿Tiene las 4 columnas pedidas?|Sí|
|¿Incluye el bloqueo después de 3 intentos?|Sí|
|¿Incluye casos con campos vacíos?|Sí|
|¿Indica qué casos agregó en la autocrítica?|Sí|
|¿Hay algún caso repetido o que no tenga sentido?|No|

```text
<rol>Actua como analista de pruebas de software.</rol>

<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>

<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

Revisa tu tabla: faltan casos limite como campos vacios, correo sin @

o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
