# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting. Herramienta de IA usada: ChatGPT

##	Ejercicio	2:	Zero-shot, one-shot y few-shot


### Prueba 1: Zero-shot

**Técnica utilizada:** Zero-shot prompting.

**Prompt utilizado:**

Clasifica estos comentarios de clientes:

1. Me encanto, llego rapido
2. No lo recomiendo
3. Es aceptable por el precio
4. Pesima atencion, no vuelvo
5. Excelente calidad, lo volveria a comprar

**Resultado obtenido:**

| N.º | Clasificación |
|---|---|
| 1 | Positivo |
| 2 | Negativo |
| 3 | Neutral |
| 4 | Negativo |
| 5 | Positivo |

**Análisis:**

Al utilizar la técnica Zero-shot, observé que ChatGPT logró clasificar correctamente los cinco comentarios sin necesidad de proporcionarle ejemplos. Además, presentó una tabla con las clasificaciones y sus justificaciones.

El resultado fue de dos comentarios positivos (40 %), dos negativos (40 %) y uno neutral (20 %).

**Conclusión:**

Comprobé que la técnica Zero-shot puede ser suficiente para realizar tareas sencillas y conocidas por el modelo. Sin embargo, no permite controlar completamente el formato de respuesta cuando no se especifican instrucciones adicionales.


### Prueba 2: One-shot

**Técnica utilizada:** One-shot prompting.

**Prompt utilizado:**

Clasifica los comentarios de clientes como Positivo, Negativo o Neutral.

Ejemplo:
Comentario: El producto es excelente.
Clasificación: Positivo.

Ahora clasifica estos comentarios:

1. Me encanto, llego rapido
2. No lo recomiendo
3. Es aceptable por el precio
4. Pesima atencion, no vuelvo
5. Excelente calidad, lo volveria a comprar

**Resultado obtenido:**

| N.º | Clasificación |
|---|---|
| 1 | Positivo |
| 2 | Negativo |
| 3 | Neutral |
| 4 | Negativo |
| 5 | Positivo |

**Análisis:**

Al aplicar la técnica One-shot, proporcioné un ejemplo antes de solicitar la clasificación de los cinco comentarios.

Observé que ChatGPT respondió correctamente los cinco casos y presentó una lista numerada con respuestas breves y directas.

A diferencia de Zero-shot, la respuesta no incluyó una tabla de justificaciones ni un resumen porcentual.

**Conclusión:**

Comprobé que proporcionar un ejemplo permite orientar la forma en que ChatGPT presenta sus respuestas. En esta prueba, la precisión fue del 100 %, igual que en Zero-shot, pero el formato fue más sencillo.


### Prueba 3: Few-shot

**Técnica utilizada:** Few-shot prompting.

**Prompt utilizado:**

Clasifica los comentarios de clientes como Positivo, Negativo o Neutral.

Ejemplos:

Comentario: El producto es excelente.
Clasificación: Positivo.

Comentario: El servicio fue muy malo.
Clasificación: Negativo.

Comentario: El producto cumple con lo esperado.
Clasificación: Neutral.

Ahora clasifica estos comentarios:

1. Me encanto, llego rapido
2. No lo recomiendo
3. Es aceptable por el precio
4. Pesima atencion, no vuelvo
5. Excelente calidad, lo volveria a comprar

**Resultado obtenido:**

| N.º | Comentario | Clasificación |
|---|---|---|
| 1 | Me encantó, llegó rápido | Positivo |
| 2 | No lo recomiendo | Negativo |
| 3 | Es aceptable por el precio | Neutral |
| 4 | Pésima atención, no vuelvo | Negativo |
| 5 | Excelente calidad, lo volvería a comprar | Positivo |

**Análisis:**

En esta tercera prueba utilicé la técnica Few-shot,
proporcionando tres ejemplos de clasificación antes
de solicitar la evaluación de los comentarios.

Observé que ChatGPT clasificó correctamente los
cinco comentarios y presentó las respuestas de
manera ordenada y directa.

Los ejemplos permitieron mostrar previamente
las tres categorías que debía utilizar el modelo.

**Conclusión:**

Comprobé que la técnica Few-shot permite orientar
al modelo mediante varios ejemplos.

En esta prueba obtuve cinco respuestas correctas,
aunque no se observó una mejora en la precisión
respecto a Zero-shot y One-shot.

### Comparación de las tres técnicas

| Criterio | Zero-shot | One-shot | Few-shot |
|---|---|---|---|
| Ejemplos | 0 | 1 | 3 |
| Respuestas correctas | 5 | 5 | 5 |
| Precisión | 100 % | 100 % | 100 % |
| Formato | Tabla | Lista | Lista |

### Conclusión general del Ejercicio 2

Después de realizar las tres pruebas, pude
comprobar que un mismo modelo de inteligencia
artificial puede presentar sus respuestas de
diferentes maneras dependiendo de cómo se
redacte el prompt.

En Zero-shot no proporcioné ejemplos y obtuve
una respuesta detallada con una tabla y un resumen.

En One-shot incluí un ejemplo y recibí una
clasificación más breve.

Finalmente, en Few-shot proporcioné tres ejemplos
y obtuve una lista ordenada con las cinco
clasificaciones correctas.

Concluyo que los ejemplos ayudan a orientar
las respuestas del modelo, aunque en este
ejercicio las tres técnicas tuvieron la misma
precisión.

##	Ejercicio	3:	Chain of Thought

### Objetivo
Comparar una respuesta directa con una respuesta que muestra
los cálculos paso a paso para resolver un problema matemático.

### Prueba 1: Pedido directo

**Prompt utilizado:**

```text
Un producto cuesta S/ 120. La tienda aplica un descuento del 25 %
y luego suma el 18 % de IGV sobre el precio con descuento.
Un cliente compra 3 unidades. Cuanto paga en total?
Responde solo con el numero.
```

**Respuesta obtenida:** 318.60

**Observación:** La IA respondió correctamente, pero no mostró
las operaciones utilizadas para obtener el resultado.

### Prueba 2: Pedido paso a paso

**Prompt utilizado:**

```text
Un producto cuesta S/ 120. La tienda aplica un descuento del 25 %
y luego suma el 18 % de IGV sobre el precio con descuento.
Un cliente compra 3 unidades. Cuanto paga en total?
Resuelvelo paso a paso: muestra cada calculo y comprueba el resultado
antes de dar la respuesta final.
```

**Respuesta obtenida:** S/ 318,60

**Observación:** La IA presentó los cálculos del descuento,
el IGV y el costo total de las tres unidades. Además,
comprobó el resultado mediante otra operación.

### Comparación de resultados

| Pedido | Respuesta de la IA | Muestra los pasos (Sí/No) | Correcta (Sí/No) |
|---|---|---|---|
| Directo | S/ 318,60 | No | Sí |
| Paso a paso | S/ 318,60 | Sí | Sí |

### Verificación del resultado

| Paso | Operación | Resultado |
|---|---|---|
| Precio con descuento | 120 × 0,75 | S/ 90,00 |
| Precio con IGV | 90 × 1,18 | S/ 106,20 |
| Total por 3 unidades | 106,20 × 3 | S/ 318,60 |

### Análisis personal

Considero que solicitar los cálculos paso a paso es útil
porque me permite verificar cómo se obtuvo el resultado
e identificar posibles errores en las operaciones.

Aunque el pedido directo también fue correcto, la segunda
respuesta fue más completa y fácil de comprobar.

##	Ejercicio	4:	Role prompting

### Comparación de resultados

| Versión | Vocabulario | Usa ejemplos o código | A quién le sirve más |
|---|---|---|---|
| A. Sin rol | Sencillo | Analogía de una caja y código Python | Público general |
| B. Rol docente | Sencillo y didáctico | Comparaciones de la vida cotidiana y ejemplos educativos | Estudiantes principiantes |
| C. Rol senior | Técnico | Código Java y tipos de datos | Programadores y desarrolladores |

### Análisis de los resultados

Al realizar las tres pruebas, observé que ChatGPT respondió de manera diferente según el rol asignado.

En la versión A, sin rol, explicó el concepto de variable de forma sencilla y utilizó ejemplos en Python.

En la versión B, al asignarle el rol de profesor de programación, desarrolló una explicación más didáctica, dirigida a estudiantes que nunca habían programado.

En la versión C, al asignarle el rol de desarrollador Java senior, presentó información más técnica y ejemplos de código Java.

### Conclusión

Comprobé que el role prompting permite orientar la respuesta de la inteligencia artificial según el público al que va dirigida.

El rol no proporciona conocimientos nuevos al modelo, pero influye en el vocabulario, el enfoque y la profundidad de la explicación.

Considero que esta técnica es útil porque permite obtener respuestas más apropiadas para estudiantes principiantes o profesionales con experiencia.


##	Ejercicio	5:	Descomposicion



### A. Pedido de una sola vez

**Prompt utilizado:**

Crea un sistema de inventario para una tienda.

**Resultado obtenido:**

ChatGPT propuso un sistema llamado "Mi Inventario",
con un panel visual y funciones para registrar
productos, controlar entradas y salidas, consultar
movimientos, generar alertas y reportes.

Sin embargo, no genero codigo Java ni un diseno
de clases. En su lugar, solicito informacion
adicional sobre el tipo de sistema, tienda
y usuarios.

**Observacion:**

El pedido general produjo una propuesta amplia,
pero no una solucion programada. La IA necesito
mas informacion para continuar con el desarrollo.


### B. Pedido por pasos

#### Paso 1: Identificacion de requisitos

**Prompt utilizado:**

Voy a crear un sistema de inventario para una
tienda pequena en Java. Lista los 5 requisitos
principales del sistema.

**Resultado obtenido:**

ChatGPT identifico cinco requisitos principales:

1. Gestion de productos.
2. Control de entradas y salidas de inventario.
3. Gestion de proveedores.
4. Alertas de stock minimo.
5. Generacion de reportes.

Tambien recomendo tecnologias como Java,
MySQL, JDBC y Swing.

**Observacion:**

A diferencia del pedido general, esta respuesta
fue mas especifica porque se indico el lenguaje
de programacion y se solicitaron exactamente
cinco requisitos.

La IA organizo las funcionalidades principales,
lo que facilita continuar con el diseno del sistema.


#### Paso 2: Diseno de clases

**Prompt utilizado:**

Con esos requisitos, disena las clases necesarias.
Para cada clase indica sus atributos con su
tipo de dato.

**Resultado obtenido:**

ChatGPT propuso seis clases principales:

1. Producto.
2. Proveedor.
3. MovimientoInventario.
4. Usuario.
5. AlertaStock.
6. Reporte.

Para cada clase identifico atributos y tipos
de datos como int, String, double, boolean
y LocalDateTime.

Tambien propuso cinco clases de servicio,
las relaciones entre las clases, un diagrama
general y una estructura de carpetas.

**Observacion:**

La IA utilizo los requisitos del paso anterior
para organizar el sistema mediante programacion
orientada a objetos.

En comparacion con el pedido general, ahora
obtuve un diseno mas detallado que permite
identificar las clases y los datos necesarios
antes de comenzar a programar.


#### Paso 3: Generacion del codigo Java

**Prompt utilizado:**

Escribe el codigo Java de la clase Producto con sus
atributos, un constructor y los metodos get y set.

**Resultado obtenido:**

ChatGPT genero el codigo Java de la clase Producto
utilizando el diseno realizado en el paso anterior.

El codigo contiene:

- Diez atributos privados.
- Un constructor para inicializar los atributos.
- Metodos get para consultar los valores.
- Metodos set para modificar los valores.
- Un ejemplo de uso mediante la clase Main.

**Observacion:**

La IA mantuvo la relacion con el diseno del Paso 2
y utilizo conceptos de programacion orientada a
objetos, como clases, atributos, constructores
y encapsulamiento.

Al dividir el trabajo en pasos, pude obtener un
codigo mas especifico y relacionado con los
requisitos del sistema de inventario.

**Estado:**

Codigo generado y revisado visualmente.
Compilacion pendiente de verificar.


#### Paso 4: Revision y mejora del codigo

**Prompt utilizado:**

Revisa el codigo de la clase Producto y propone
3 mejoras concretas.

**Resultado obtenido:**

ChatGPT reviso el codigo generado anteriormente
y propuso las siguientes mejoras:

1. Cambiar el tipo de dato double por BigDecimal
   para mejorar la precision de los precios.

2. Implementar validaciones en los metodos set
   para evitar registrar precios o cantidades
   negativas.

3. Agregar el metodo tieneStockBajo() para
   identificar productos que necesitan reposicion.

**Observacion:**

La IA utilizo el codigo del Paso 3 como referencia
para identificar aspectos que podrian mejorarse.

Las recomendaciones fueron concretas y estuvieron
acompanadas de ejemplos de codigo Java.

**Conclusion del paso:**

Comprendi que la descomposicion permite revisar
y mejorar cada parte de una solucion antes de
continuar con el desarrollo del sistema.


### Comparacion de resultados

Al realizar el pedido general, ChatGPT me
proporciono una descripcion de los requisitos
principales del sistema de inventario y algunas
tecnologias recomendadas. Sin embargo, no
desarrollo directamente el codigo Java.

Cuando dividi la tarea en cuatro pasos, obtuve
resultados mas especificos. Primero identifique
los requisitos, despues consegui el diseno de
clases, luego el codigo de la clase Producto y,
finalmente, tres propuestas de mejora.

### Conclusion del Ejercicio 5

En este ejercicio aprendi que la tecnica de
descomposicion consiste en dividir una tarea
grande en solicitudes mas pequenas y ordenadas.

Considero que esta tecnica es util porque permite
revisar los resultados de la inteligencia
artificial antes de avanzar al siguiente paso.

Tambien observe que las respuestas mantienen
relacion entre si cuando se trabaja en el mismo
chat, lo que ayuda a desarrollar una solucion
mas organizada y coherente.

##	Ejercicio	6:	Prompt estructurado y autocritica



### Paso 1: Prompt basico

**Prompt utilizado:**

Dame casos de prueba para un login.

**Resultado obtenido:**

ChatGPT genero 34 casos de prueba para un
sistema de inicio de sesion, organizados
en cinco categorias:

- 8 casos de pruebas funcionales.
- 8 casos de pruebas de validacion.
- 6 casos de pruebas de seguridad.
- 6 casos de pruebas de interfaz y usabilidad.
- 6 casos de pruebas adicionales.

Ademas, presento un ejemplo detallado del
caso CP-001 y recomendaciones para elaborar
una matriz de pruebas QA.

**Observacion:**

La respuesta fue bastante completa a pesar
de que el prompt era general. Sin embargo,
no indique la cantidad de pruebas, las
caracteristicas del sistema ni el formato
que necesitaba.

Observe que ChatGPT asumio algunas
funcionalidades del login, por lo que
seria necesario verificar si realmente
existen en el sistema que se va a probar.

```text
(### Prompt estructurado

**Prompt utilizado:**

<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

**Resultado obtenido:**

ChatGPT genero 6 casos de prueba en una tabla con las cuatro columnas solicitadas. Los escenarios incluyeron el acceso correcto, credenciales incorrectas, intentos fallidos consecutivos y bloqueo de la cuenta despues del tercer intento.



### Autocritica

**Prompt utilizado:**

Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.

**Resultado obtenido:**

ChatGPT reviso la tabla anterior y reconocio que faltaban casos limite. Agrego 8 casos nuevos, pasando de 6 a 14 pruebas.

| ID | Caso nuevo agregado |
|---|---|
| CP-007 | Ambos campos vacios |
| CP-008 | Correo vacio |
| CP-009 | Contrasena vacia |
| CP-010 | Correo sin simbolo @ |
| CP-011 | Correo con formato incompleto |
| CP-012 | Contrasena con espacios al inicio o al final |
| CP-013 | Contrasena formada solo por espacios |
| CP-014 | Correo con espacios al inicio o al final |

### Comparacion de resultados

El prompt inicial genero una respuesta extensa con 34 casos generales. En cambio, el prompt estructurado produjo 6 casos enfocados en un login web con bloqueo despues de tres intentos fallidos. Finalmente, la autocritica permitio identificar situaciones que no se habian considerado y agregar 8 pruebas nuevas.

### Conclusion del Ejercicio 6

En este ejercicio aprendi que un prompt estructurado ayuda a obtener respuestas mas precisas porque permite indicar el rol, el contexto, la tarea y el formato esperado. Tambien comprobe que pedir a la inteligencia artificial que revise su propia respuesta ayuda a detectar omisiones y mejorar el resultado. Sin embargo, los casos propuestos deben verificarse con los requisitos reales del sistema antes de utilizarlos.
  

### Evaluacion de la tabla final

| Que revisar | Cumple (Si / No) |
|---|:---:|
| Tiene las 4 columnas pedidas? | Si |
| Incluye el bloqueo despues de 3 intentos? | Si |
| Incluye casos con campos vacios? | Si |
| Indica que casos agrego en la autocritica? | Si |
| Hay algun caso repetido o que no tenga sentido? | No |

**Observacion:**

Al revisar la tabla final, comprobe que cumple con las cuatro columnas solicitadas y considera el bloqueo de la cuenta despues de tres intentos fallidos. Tambien incluye pruebas con campos vacios e identifica los ocho casos agregados durante la autocritica. No encontre casos repetidos ni escenarios que no tuvieran sentido. Considero que la revision permitio mejorar la cobertura de las pruebas del login.
  
)
```

### Evaluacion de la tabla final

| Que revisar | Cumple (Si / No) |
|---|:---:|
| Tiene las 4 columnas pedidas? | Si |
| Incluye el bloqueo despues de 3 intentos? | Si |
| Incluye casos con campos vacios? | Si |
| Indica que casos agrego en la autocritica? | Si |
| Hay algun caso repetido o que no tenga sentido? | No |

**Observacion:**

Al revisar la tabla final, comprobe que cumple con las cuatro columnas solicitadas y considera el bloqueo de la cuenta despues de tres intentos fallidos. Tambien incluye pruebas con campos vacios e identifica los ocho casos agregados durante la autocritica. No encontre casos repetidos ni escenarios que no tuvieran sentido. Considero que la revision permitio mejorar la cobertura de las pruebas del login.
  
