# Tarea: Mi prompt avanzado

## Tarea elegida

Diseñar las clases de un sistema de notas para estudiantes en Java.

## Version 1: prompt basico

```text
Diseña las clases para un sistema de notas de estudiantes en Java.
```

La respuesta propuso las clases Estudiante, Curso, Nota, Docente y SistemaNotas, con sus atributos y relaciones.

## Version 2

```text
<rol>
Actúa como desarrollador Java especializado en diseño de sistemas académicos.
</rol>

<contexto>
Estoy creando un sistema de notas para estudiantes en Java.
El sistema debe permitir registrar estudiantes, cursos y sus notas.
</contexto>

<tarea>
Diseña las clases necesarias para el sistema.
Para cada clase indica su responsabilidad, atributos y tipos de datos.
También explica cómo se relacionan las clases entre sí.
</tarea>

<formato>
Presenta la información en una tabla con las columnas:
Clase, responsabilidad, atributo y tipo de dato.

Después de la tabla, explica brevemente las relaciones entre las clases.
</formato>
```

**Técnicas agregadas:** Role prompting y Structured prompt.

**¿Por qué?** Para indicar el rol de la IA y organizar mejor la información que debe entregar.

**¿Qué mejoró?** La respuesta fue más ordenada, específica y explicó mejor las relaciones entre las clases.

## Version 3: prompt final

```text
Actúa como desarrollador Java especializado en sistemas académicos.

Estoy creando un sistema de notas para estudiantes en Java.
Diseña las clases necesarias e indica para cada una:
- responsabilidad
- atributos
- tipo de dato de los atributos
- relaciones con otras clases

Organiza la respuesta en una tabla con las columnas:
Clase | Responsabilidad | Atributos y tipos | Relaciones

Al finalizar, revisa tu propuesta y comprueba que:
1. No haya clases repetidas o innecesarias.
2. Todos los atributos tengan un tipo de dato.
3. Las relaciones entre las clases sean coherentes.
4. El diseño sea sencillo de implementar en Java.

Si encuentras algún problema, corrígelo antes de mostrar la respuesta final.
```

**Técnicas utilizadas:** Role prompting, Structured prompt y Self-critique.

**¿Qué mejoró?** La respuesta mantuvo un diseño sencillo, organizó la información en una tabla y agregó una revisión final de la propuesta.

## Tecnicas usadas en el prompt final

| Técnica           | Uso                                                 |
| ----------------- | --------------------------------------------------- |
| Role prompting    | Define el rol de desarrollador Java.                |
| Structured prompt | Organiza la tarea y define el formato.              |
| Self-critique     | Revisa la propuesta antes de entregar la respuesta. |

## Evaluacion del resultado

| Criterio                       | Cumple |
| ------------------------------ | ------ |
| Usa al menos 3 técnicas        | Sí     |
| Tiene un rol específico        | Sí     |
| Define un formato de respuesta | Sí     |
| Incluye autocrítica            | Sí     |

## Por que elegi estas tecnicas

Elegí estas técnicas porque permiten obtener una respuesta más organizada y específica. El Role prompting define el rol de la IA, el Structured prompt organiza la información y el Self-critique permite revisar la propuesta antes de mostrarla.
