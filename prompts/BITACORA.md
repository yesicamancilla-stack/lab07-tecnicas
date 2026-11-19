# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Sí/No) |
|---|---|---|---|
| Zero-shot | 5/5 | Texto entre comillas, flecha y clasificación | Sí |
| One-shot | 5/5 | Texto entre comillas, flecha y clasificación | Sí |
| Few-shot | 5/5 | Texto entre comillas, flecha y clasificación | Sí |

Observación: Las tres técnicas lograron 5 aciertos.
Few-shot mantuvo un formato uniforme en las
clasificaciones, aunque agregó un comentario
adicional que no fue solicitado.

## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Sí/No) | Correcta (Sí/No) |
|---|---|---|---|
| Directo | S/ 318,60 | No | Sí |
| Paso a paso | S/ 318,60 | Sí | Sí |

### Comprobación del resultado

1. Precio con descuento: 120 × 0,75 = S/ 90,00.
2. Precio con IGV: 90 × 1,18 = S/ 106,20.
3. Total por 3 unidades: 106,20 × 3 = S/ 318,60.

### Observación

Mostrar los cálculos paso a paso permite verificar
que el descuento y el IGV se aplicaron correctamente.
Aunque la respuesta directa sea correcta, explicar
el procedimiento facilita identificar posibles errores.


## Ejercicio 4: Role prompting

| Versión | Vocabulario (sencillo/técnico) | Usa ejemplos o código | A quién le sirve más |
|---|---|---|---|
| A. Sin rol | Sencillo y general | Ejemplos básicos | Personas con conocimientos básicos de programación |
| B. Rol docente | Sencillo y didáctico | Ejemplos cotidianos, como una caja que guarda datos | Estudiantes que recién empiezan a programar |
| C. Rol senior | Técnico y especializado | Ejemplos de código Java y tipos de datos | Programadores con experiencia |

### Comparación de resultados

La versión sin rol ofrece una explicación general.
El rol docente facilita la comprensión mediante ejemplos
cotidianos. El rol senior utiliza conceptos técnicos
y ejemplos de código Java.


## Ejercicio 5: Descomposicion

### Registro de resultados

| Paso | Resultado obtenido |
|---|---|
| Pedido de una sola vez | La IA presentó una propuesta general de un sistema de inventario, sin especificar todos los requisitos. |
| Paso 1: Requisitos | Se identificaron cinco requisitos principales para gestionar el inventario de una tienda. |
| Paso 2: Diseño de clases | Se propusieron clases para el sistema, indicando sus atributos y tipos de datos. |
| Paso 3: Código Java | Se desarrolló la clase Producto con atributos, constructor y métodos get y set. |
| Paso 4: Mejoras | Se propusieron tres mejoras para fortalecer las validaciones y la organización del código. |

### Comparación

El pedido de una sola vez generó una respuesta general
y menos organizada. En cambio, la descomposición permitió
desarrollar el sistema por etapas, obteniendo requisitos,
diseño de clases, código Java y propuestas de mejora
de manera más ordenada.


## Ejercicio 6: Prompt estructurado y autocritica


### Prompt básico

Dame casos de prueba para un login.

### Prompt estructurado

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>
```

### Prompt de autocrítica

```text
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```

### Evaluación del resultado

| Qué revisar | Cumple (Sí/No) |
|---|---|
| ¿Tiene las 4 columnas pedidas? | Sí |
| ¿Incluye el bloqueo después de 3 intentos? | Sí |
| ¿Incluye casos con campos vacíos? | Sí |
| ¿Indica qué casos agregó en la autocrítica? | Sí |
| ¿Hay algún caso repetido o que no tenga sentido? | No |

### Observación

El prompt estructurado permite obtener casos de prueba
organizados y específicos. La autocrítica ayuda a
identificar escenarios que no se consideraron
inicialmente, como campos vacíos o datos inválidos.
