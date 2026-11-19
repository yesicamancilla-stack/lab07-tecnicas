
# Tarea: Mi prompt avanzado

## Tarea elegida

Generación de casos de prueba para el registro de
productos de TiendaTec, una aplicación de escritorio
desarrollada en Java.

## Version 1: prompt basico

```text
Genera casos de prueba para el registro de productos
de una aplicación de escritorio desarrollada en Java
llamada TiendaTec.

Los productos tienen código, nombre, precio y stock.
```

### Técnica utilizada
Prompt básico, sin técnicas avanzadas.

### Resultado y aspectos por mejorar
Permite obtener casos de prueba generales, pero no
establece un rol específico ni un formato obligatorio.
Se necesita mayor precisión en las validaciones.

## Version 2

### Prompt mejorado

```text
Actúa como analista de pruebas de software
especializado en aplicaciones Java Swing.

Genera 6 casos de prueba para el registro de
productos de TiendaTec.

Cada producto tiene código, nombre, precio y stock.

Presenta los resultados en una tabla con las columnas:
ID, escenario, datos de entrada y resultado esperado.

Incluye pruebas con datos válidos e inválidos.
```

### Técnicas agregadas

Role prompting y definición del formato de respuesta.

### ¿Por qué se agregaron?

Se asignó un rol específico para orientar la respuesta
hacia las pruebas de software. Además, se definió una
estructura para organizar los casos de prueba.

### ¿Qué mejoró?

Se espera obtener una tabla más organizada, con casos
de prueba específicos y resultados esperados claros.

## Version 3: prompt final

### Prompt avanzado

```text
<rol>
Actúa como analista QA especializado en pruebas
funcionales de aplicaciones Java Swing.
</rol>

<contexto>
TiendaTec es una aplicación de escritorio en Java
para gestionar productos de una tienda.

Cada producto contiene:
- Código: obligatorio y único.
- Nombre: obligatorio y no vacío.
- Precio: mayor que cero.
- Stock: número entero mayor o igual que cero.
</contexto>

<ejemplos>
CP01 | Registro válido | Código P001, nombre Mouse,
precio 50, stock 10 | Producto registrado correctamente.

CP02 | Precio negativo | Código P002, nombre Teclado,
precio -20, stock 5 | Registro rechazado.

CP03 | Nombre vacío | Código P003, nombre vacío,
precio 80, stock 4 | Solicita ingresar un nombre.
</ejemplos>

<tarea>
Genera 8 casos de prueba nuevos sin repetir los ejemplos.
Incluye datos válidos, inválidos y casos límite.

Revisa tu respuesta antes de finalizar para identificar
escenarios faltantes, inconsistencias o casos repetidos.
</tarea>

<formato>
Presenta una tabla con las columnas:
ID, escenario, datos de entrada y resultado esperado.

Responde en español e indica qué casos límite incluiste.
</formato>
```

### Técnicas agregadas

Few-shot, prompt estructurado y autocrítica,
manteniendo el role prompting de la versión anterior.

### ¿Por qué se agregaron?

Los ejemplos permiten establecer un formato de referencia.
Las etiquetas organizan las instrucciones y la autocrítica
permite revisar posibles errores o casos faltantes.

### ¿Qué mejoró?

El prompt final busca generar pruebas más completas,
con validaciones, casos límite y una revisión de
los resultados antes de presentar la respuesta.



## Tecnicas usadas en el prompt final

| Técnica | Parte del prompt |
|---|---|
| Role prompting | Etiqueta rol, que asigna el papel de analista QA |
| Few-shot | Etiqueta ejemplos, con tres casos de referencia |
| Prompt estructurado | Etiquetas rol, contexto, ejemplos, tarea y formato |
| Autocrítica | Instrucción de revisar errores, inconsistencias y casos repetidos |

## Evaluacion del resultado

| Criterio | Cumple (Sí/No) |
|---|---|
| Presenta las cuatro columnas solicitadas | Sí |
| Genera ocho casos de prueba nuevos | Síya  |
| Incluye datos válidos e inválidos | Sí |
| Incluye casos límite | Sí |
| Evita repetir los ejemplos proporcionados | Sí |
| Mantiene el formato solicitado | Sí |

## Por que elegi estas tecnicas

Elegí estas técnicas porque permiten mejorar la calidad
de los casos de prueba para TiendaTec. El role prompting
orienta la respuesta hacia el análisis de pruebas, mientras
que few-shot proporciona ejemplos del formato esperado.
El prompt estructurado organiza las instrucciones y la
autocrítica ayuda a identificar posibles errores. Estas
técnicas resultan útiles para obtener casos de prueba
más precisos y organizados para el registro de productos.
