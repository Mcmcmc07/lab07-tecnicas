# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: ChatGPT

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta   | Todas con el mismo formato (Si/No) |
| --------- | --------------- | ------------------------- | ---------------------------------- |
| Zero-shot | 5               | Tabla + resumen           | No                                 |
| One-shot  | 5               | Lista numerada            | No                                 |
| Few-shot  | 5               | Lista "texto" -> etiqueta | Sí                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA                       | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ---------------------------------------- | ------------------------- | ---------------- |
| Directo     | 318.60                                   | No                        | Sí               |
| Paso a paso | Muestra los cálculos y llega a S/ 318.60 | Sí                        | Sí               |

Ver los pasos permite comprobar cómo la IA llegó a la respuesta y detectar en qué cálculo podría estar un error Aunque la respuesta directa sea correcta, revisar el procedimiento ayuda a verificar el resultado y entender el proceso.

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas                      |
| -------------- | ------------------------------ | --------------------- | ----------------------------------------- |
| A. Sin rol     | Sencillo                       | Sí                    | Cualquier persona                         |
| B. Rol docente | Sencillo                       | Sí                    | Estudiantes, aprendices                   |
| C. Rol senior  | Técnico                        | Sí                    | Desarrolladores, personas con experiencia |

## Ejercicio 5: Descomposicion

Se creó el archivo Producto.java dentro de la carpeta src. Al compilarlo se presentó un problema con la configuración de Java, por lo que se utilizó directamente el JDK 17 instalado en el equipo.

La compilación se realizó correctamente y se generó el archivo
Producto.class.

El pedido por pasos permitió obtener primero los requisitos, luego diseñar las clases y finalmente crear y revisar el código de Producto.
En comparación, el pedido de una sola vez genera una respuesta más general.

## Ejercicio 6: Prompt estructurado y autocritica

### Tabla de evaluación

| Qué revisar                                      | Cumple (Sí / No) |
| ------------------------------------------------ | ---------------- |
| ¿Tiene las 4 columnas pedidas?                   | Sí               |
| ¿Incluye el bloqueo después de 3 intentos?       | Sí               |
| ¿Incluye casos con campos vacíos?                | Sí               |
| ¿Indica qué casos agregó en la autocrítica?      | Sí               |
| ¿Hay algún caso repetido o que no tenga sentido? | No               |

### Prompt y autocrítica

```text
1. Prompt estructurado

<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>

2. Mensaje de autocrítica

Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
