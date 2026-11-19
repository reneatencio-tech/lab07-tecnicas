
# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para un sistema de gestion de inventario de una tienda desarrollado en Java.

## Version 1: prompt basico

### Prompt utilizado

Genera casos de prueba para un sistema de inventario de una tienda desarrollado en Java.

### Resultado obtenido

La inteligencia artificial genero 36 casos de prueba:

- Registro de productos: 7 casos.
- Consulta de productos: 5 casos.
- Actualizacion de productos: 6 casos.
- Eliminacion de productos: 4 casos.
- Control de inventario: 8 casos.
- Pruebas no funcionales: 6 casos.

Ademas, incluyo ejemplos de codigo Java, pruebas unitarias
con JUnit 5, una matriz resumen y recomendaciones de
herramientas para realizar pruebas.

### Evaluacion

La respuesta fue completa, pero demasiado extensa.
La inteligencia artificial incluyo algunas funcionalidades
que no habia especificado en el prompt.

Comprendi que una instruccion general puede generar
bastante informacion, pero no necesariamente adaptada
a las necesidades reales de mi proyecto.

Considero que el prompt necesita mayor precision para
obtener casos de prueba concretos y faciles de evaluar.


## Versión 2: prompt avanzado

### Técnica utilizada

Para mejorar el resultado, utilicé un prompt estructurado que incluye un rol especializado, el contexto del sistema, una tarea específica, el formato de respuesta y restricciones.

### Prompt utilizado

Actúa como especialista en pruebas de software con experiencia en aplicaciones Java.

**Contexto:** Estoy desarrollando un sistema de inventario para una tienda pequeña. El sistema permite registrar productos, consultar productos por código, actualizar precio y stock, eliminar productos y calcular el valor total del inventario. Cada producto tiene código, nombre, precio y stock.

**Tarea:** Genera exactamente 10 casos de prueba funcionales para verificar estas operaciones. Incluye situaciones correctas y situaciones de error, como códigos duplicados, productos inexistentes, precios negativos y stock insuficiente.

**Formato:** Presenta los resultados en una tabla Markdown con cuatro columnas: ID, Caso de prueba, Datos de entrada y Resultado esperado.

**Restricciones:** No generes código Java ni agregues funcionalidades que no estén descritas. Utiliza explicaciones breves y claras.

### Resultado obtenido

La inteligencia artificial generó exactamente 10 casos de prueba funcionales, organizados de la siguiente manera:

| ID | Caso de prueba |
|---|---|
| CP-01 | Registrar un producto correctamente |
| CP-02 | Registrar un producto con código duplicado |
| CP-03 | Consultar un producto existente por código |
| CP-04 | Consultar un producto inexistente |
| CP-05 | Actualizar correctamente el precio de un producto |
| CP-06 | Actualizar un producto con precio negativo |
| CP-07 | Actualizar el stock de un producto |
| CP-08 | Eliminar un producto existente |
| CP-09 | Intentar eliminar un producto inexistente |
| CP-10 | Calcular el valor total del inventario |

La respuesta respetó el formato solicitado de cuatro columnas: ID, Caso de prueba, Datos de entrada y Resultado esperado.

También incluyó ejemplos de operaciones correctas y situaciones de error. Sin embargo, no presentó un caso específico de stock insuficiente, a pesar de que estaba solicitado en el prompt.

### Análisis del resultado

Observé que la respuesta fue más breve y enfocada en las funcionalidades del sistema de inventario. La inteligencia artificial respetó la cantidad de casos solicitados y evitó generar código Java innecesario.

El resultado fue más fácil de revisar porque cada caso de prueba tenía un identificador, los datos de entrada y el resultado esperado.

No obstante, identifiqué que la respuesta omitió una situación solicitada: el stock insuficiente. Por ello, considero importante revisar siempre los resultados generados por la inteligencia artificial.

## Versión 3: Prompt avanzado con autocrítica

### Técnica utilizada

En esta versión utilicé la técnica de autocrítica, que consiste en solicitar a la inteligencia artificial que revise su respuesta anterior, identifique posibles errores y proponga mejoras.

### Prompt propuesto

Revisa críticamente los 10 casos de prueba que acabas de generar para el sistema de inventario en Java.

1. Identifica si todos los casos cumplen con las funcionalidades y restricciones solicitadas.
2. Detecta casos omitidos, repetidos o poco claros, prestando especial atención al manejo de stock insuficiente.
3. Explica brevemente las deficiencias encontradas.
4. Presenta una versión corregida y mejorada con exactamente 10 casos de prueba, manteniendo las cuatro columnas: ID, Caso de prueba, Datos de entrada y Resultado esperado.
5. Indica cuáles casos modificaste o reemplazaste y por qué.

No generes código Java ni agregues funcionalidades que no pertenezcan al sistema descrito.

### Resultado simulado

Debido a las limitaciones se elaboró una simulación del resultado esperado de la autocrítica, tomando como referencia la respuesta real obtenida en la Versión 2.

En esta simulación, la inteligencia artificial identifica que la respuesta anterior cumplía con la cantidad de casos y el formato solicitado, pero había omitido una prueba relacionada con el stock insuficiente.

Como mejora, se propone reemplazar el caso CP-07 por una prueba que compruebe el rechazo de un retiro superior a las existencias disponibles.

### Evaluación de la respuesta simulada

| Criterio | Resultado |
|---|---|
| Presenta exactamente 10 casos | Sí |
| Mantiene las cuatro columnas | Sí |
| Identifica una omisión de la respuesta anterior | Sí |
| Propone un caso de stock insuficiente | Sí |
| Explica qué caso fue modificado | Sí |
| Genera código Java innecesario | No |

### Análisis

Esta simulación me permitió comprender cómo la autocrítica puede ayudar a detectar errores u omisiones en una respuesta generada por inteligencia artificial.

En la Versión 2 se obtuvo una respuesta más precisa que en el prompt básico, pero todavía faltaba un caso solicitado. Mediante la autocrítica se puede identificar esa omisión y proponer una corrección.

También aprendí que las mejoras propuestas deben comprobarse con los requisitos reales del sistema, porque la inteligencia artificial puede asumir funcionalidades que no han sido implementadas.

## Comparación de las tres versiones

Al comparar las tres versiones, observé que la manera de redactar un prompt influye directamente en la respuesta obtenida.

En la primera versión utilicé una instrucción general y la inteligencia artificial generó 36 casos de prueba, además de código Java y recomendaciones adicionales. Aunque la información era útil, resultó más extensa de lo necesario.

En la segunda versión incorporé un rol, contexto, instrucciones específicas, formato y restricciones. Como resultado, obtuve exactamente 10 casos de prueba organizados en una tabla de cuatro columnas. Sin embargo, identifiqué que faltaba una prueba de stock insuficiente.

En la tercera versión desarrollé una simulación de autocrítica para demostrar cómo se podría detectar esa omisión y corregirla. Esta comparación me permitió reconocer la importancia de revisar las respuestas y verificar que cumplan con todos los requisitos.

## Conclusión de la tarea

Con esta actividad aprendí que un prompt bien estructurado permite obtener respuestas más claras, precisas y útiles para el desarrollo de software.

También comprendí que no basta con indicar qué queremos obtener. Es importante definir el contexto, el formato y las restricciones, así como revisar posteriormente los resultados.

Finalmente, la técnica de autocrítica me permitió comprender cómo identificar omisiones y plantear mejoras. Considero que estas técnicas pueden ayudarme a utilizar la inteligencia artificial de manera más organizada en mis proyectos de programación.

**Nota:** Los resultados de las versiones 1 y 2 corresponden a respuestas reales observadas. La Versión 3 se presenta como una simulación didáctica y no como una respuesta ejecutada y verificada.

## Tecnicas usadas en el prompt final

Para desarrollar mi prompt avanzado utilicé las siguientes técnicas:

1. **Role Prompting:** Asigné a la inteligencia artificial el rol de especialista en pruebas de software con experiencia en Java, para orientar la respuesta hacia un contexto profesional.

2. **Prompt estructurado:** Organicé las instrucciones indicando el contexto del sistema de inventario, la tarea que debía realizar, el formato de presentación y las restricciones.

3. **Especificación del formato:** Solicité exactamente 10 casos de prueba en una tabla Markdown con cuatro columnas: ID, Caso de prueba, Datos de entrada y Resultado esperado.

4. **Autocrítica:** Planteé una revisión de la respuesta anterior para identificar posibles errores, casos omitidos y oportunidades de mejora.

5. **Descomposición de tareas:** Dividí el trabajo en etapas: generación inicial, elaboración de un prompt avanzado y revisión mediante autocrítica.

## Evaluacion del resultado

Al comparar los resultados, observé que la calidad de las respuestas mejoró al utilizar instrucciones más específicas.

En la primera versión, el prompt básico generó 36 casos de prueba y contenido adicional, incluyendo ejemplos de código Java. Aunque la información era útil, la respuesta resultó extensa y no estaba limitada a una cantidad determinada de casos.

En la segunda versión, el prompt avanzado generó exactamente 10 casos de prueba, respetando las cuatro columnas solicitadas y sin incluir código Java innecesario. Sin embargo, identifiqué que no se había considerado un caso específico de stock insuficiente.

Para la tercera versión, se elaboró una simulación de autocrítica en la que se identificó esta omisión y se propuso una mejora. Esta simulación permitió analizar cómo una revisión adicional podría ayudar a obtener una respuesta más completa.

Considero que el prompt avanzado fue más efectivo que el básico porque permitió controlar mejor la cantidad de información, el formato y el contenido de la respuesta.

No obstante, aprendí que siempre es necesario verificar los resultados de la inteligencia artificial antes de utilizarlos en un proyecto real.

## Por que elegi estas tecnicas

Elegí estas técnicas porque necesitaba generar casos de prueba claros y organizados para un sistema de inventario desarrollado en Java.

El Role Prompting me permitió orientar a la inteligencia artificial hacia el área de pruebas de software. El prompt estructurado me ayudó a explicar las características del sistema y establecer instrucciones concretas.

La especificación del formato fue importante porque facilitó la lectura, comparación y documentación de los casos de prueba en Markdown.

También consideré útil la descomposición de tareas, ya que me permitió desarrollar el trabajo progresivamente y revisar cada resultado antes de continuar.

Finalmente, elegí la autocrítica porque comprendí que una respuesta puede cumplir con la mayoría de las instrucciones y aun así presentar omisiones. Esta técnica permite plantear mejoras y reforzar la revisión de los resultados.

En conclusión, aprendí que combinar diferentes técnicas de prompting permite trabajar de manera más ordenada con la inteligencia artificial y obtener respuestas mejor adaptadas a las necesidades de un proyecto de programación.

