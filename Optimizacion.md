# 📚 Banco de Preguntas: Tema Optimizacion

## Pregunta 1
Un científico de datos está ajustando los hiperparámetros de un modelo de *Gradient Boosting*. Decide utilizar **PSO** para encontrar la combinación óptima de `learning_rate` y `max_depth`. Si una "partícula" se encuentra en una zona del espacio de búsqueda con un error de validación muy bajo, ¿cómo influye esto en el resto del enjambre en la siguiente iteración?  

- [ ] Las demás partículas ignoran esa posición para evitar el sobreajuste del modelo.
- [ ] La partícula en la zona óptima se detiene permanentemente para actuar como un "centroide" fijo.
- [ ] El algoritmo aumenta la inercia de todas las partículas para que exploren áreas opuestas a la zona encontrada.
- [x] **El vector de velocidad de las demás partículas se verá influenciado por la posición global mejor lograda (gbest), tirando de ellas hacia esa zona promisoria.**

**Explicación:** En el algoritmo de optimización [[PSO]] (Particle Swarm Optimization), cada partícula ajusta su trayectoria considerando su propia mejor posición pasada y la mejor posición descubierta por todo el enjambre (`gbest`). 

---

## Pregunta 2
Se desea mejorar el algoritmo K-Means usando PSO para evitar que los centroides se estanquen en mínimos locales. ¿Qué representaría la "posición" de una partícula en este enjambre?  

- [ ] La velocidad a la que los datos se agrupan en cada iteración.
- [x] **Un vector que contiene las coordenadas de todos los centroides propuestos para los clusters.**
- [ ] El número total de clusters (K) que el algoritmo debe encontrar.
- [ ] La distancia euclidiana entre el punto más lejano y el centroide más cercano.

**Explicación:** Al combinar [[PSO]] con [[K-Means]], cada partícula es una solución candidata entera para el problema, lo cual equivale a la ubicación matemática (coordenadas) de todos los $K$ centroides en el espacio de características.

---

## Pregunta 3
Un algoritmo de optimización bioinspirado utiliza una población de soluciones candidatas organizadas en tres grupos con funciones específicas:
* **Exploradoras:** buscan nuevas regiones en el espacio de soluciones sin depender de información previa.  
* **Empleadas:** exploran soluciones cercanas a las mejores encontradas.  
* **Observadoras:** seleccionan soluciones prometedoras en función de un mecanismo de evaluación basado en calidad.

El proceso de búsqueda se basa en la comunicación entre soluciones y un equilibrio entre exploración y explotación, pero sin el uso de rastros persistentes que guíen futuras búsquedas.  

- [ ] Algoritmo de Enjambre de Partículas (PSO)
- [x] **Algoritmo de Abejas (BA)**
- [ ] Algoritmo de Optimización de Colonias de Hormigas (ACO)
- [ ] Algoritmo Genético (GA)

**Explicación:** La división de roles en abejas empleadas, observadoras (onlookers) y exploradoras (scouts) es la característica distintiva del [[Algoritmo de Colonia Artificial de Abejas (ABC)]] (o Algoritmo de Abejas).

---

## Pregunta 4
Al aplicar ACO para Feature Selection, ¿cómo se decide qué variable será la siguiente en ser añadida al subconjunto por una hormiga?  

- [ ] Se elige la variable que menos feromona tenga para ser justos.
- [ ] Se elige siempre la variable con el nombre alfabéticamente primero.
- [x] **Se utiliza una regla probabilística que combina la intensidad de la feromona y una información heurística (como la ganancia de información).**
- [ ] Se eligen todas las variables disponibles para no perder información.

**Explicación:** En la [[Optimización por Colonia de Hormigas (ACO)]], las hormigas construyen soluciones paso a paso. La elección del siguiente paso se hace aleatoriamente ponderando la memoria histórica del enjambre (feromona) y el atractivo local del paso (información heurística).

---

## Pregunta 5
En la Selección de Características con ACO, ¿por qué se aplica el concepto de "evaporación de feromona"?  

- [ ] Para aumentar la velocidad de procesamiento del algoritmo en datasets grandes.
- [ ] Para eliminar las variables que consumen demasiada memoria en el servidor.
- [x] **Para permitir que el algoritmo olvide caminos mediocres y evitar la convergencia prematura hacia un subconjunto de variables subóptimo.**
- [ ] Para asegurar que todas las variables tengan la misma probabilidad de ser elegidas al final.

**Explicación:** La evaporación en [[ACO]] es crucial; actúa como un mecanismo de olvido que disminuye la feromona de todas las rutas, lo que favorece la exploración y evita que el algoritmo converja demasiado rápido en una solución subóptima ([[Convergencia prematura]]).

---

## Pregunta 6
Se tienen los siguientes padres en un algoritmo genético:
Padre 1 = "EVOLUCION"
Padre 2 = "ALGORITMO"

Después de aplicar un **cruce de un punto**, se obtienen los siguientes hijos:
Hijo 1 = "EVOLRITMO"
Hijo 2 = "ALGOUCION"

**¿En qué posición se aplicó el operador de cruce?**  

- [ ] Después de la **sexta** letra
- [ ] Después de la **tercera** letra
- [x] **Después de la cuarta letra**
- [ ] Después de la **quinta** letra

**Explicación:** En un [[Algoritmo Genético]], el [[Cruce de un punto]] combina el inicio de un padre con el final del otro. Si cortamos "EVOL|UCION" y "ALGO|RITMO" tras la 4ta letra e intercambiamos las colas, obtenemos EVOL+RITMO y ALGO+UCION.

---

## Pregunta 7
Si estamos resolviendo un **problema de asignación** de recursos, y tenemos una variable de decisión, $x_{ij}$, ¿qué representa esta variable en el contexto del modelo?  

- [ ] El costo total de asignar recursos a las tareas.
- [ ] La cantidad de tareas asignadas a un recurso.
- [ ] La cantidad de recursos disponibles.
- [x] **Si el recurso i es asignado a la tarea j (1 si asignado, 0 si no asignado).**

**Explicación:** El modelo estándar de un [[Problema de asignación]] utiliza programación entera binaria. Sus variables de decisión $x_{ij}$ toman el valor de 1 si ocurre la asignación y 0 si no ocurre.

---

## Pregunta 8
En un **problema de asignación** en el que se asignan recursos a tareas, y se cuenta con una restricción adicional que limita el número máximo de tareas que puede realizar cada recurso (por ejemplo, un trabajador solo puede realizar hasta 3 tareas), ¿cuál es la restricción correcta para modelar este escenario?  

- [x] **La suma de las asignaciones de un recurso a las tareas debe ser menor o igual al número máximo de tareas que ese recurso puede realizar.**
- [ ] La suma de las asignaciones de todos los recursos a las tareas debe ser menor o igual al número total de tareas.
- [ ] La suma de las asignaciones de un recurso a las tareas debe ser igual al número máximo de tareas que ese recurso puede realizar.
- [ ] La suma de las asignaciones de un recurso a las tareas debe ser mayor o igual al número máximo de tareas que ese recurso puede realizar.

**Explicación:** Matemáticamente esto es $\sum_j x_{ij} \le M$, que indica que para un recurso específico $i$, el total de tareas $j$ a las que es asignado no debe superar su capacidad límite $M$.

---

## Pregunta 9
En un **problema de asignación** de recursos limitados a tareas, ¿cuál sería la restricción adecuada para asegurar que no se asignen más recursos de los disponibles a las tareas?  

- [ ] La suma de las asignaciones de recursos a una tarea debe ser mayor o igual a la cantidad de recursos disponibles.
- [ ] La suma de las asignaciones de recursos a todas las tareas debe ser igual al número total de recursos.
- [ ] La suma de las asignaciones de todas las tareas a los recursos debe ser menor o igual a la cantidad de recursos disponibles.
- [x] **La suma de las asignaciones de recursos a una tarea debe ser menor o igual a la cantidad de recursos disponibles.**

**Explicación:** Esta formulación indica que la cantidad de recursos destinados a una tarea no puede sobrepasar los recursos totales que se tienen. Matemáticamente garantiza que la suma de asignaciones no exceda la oferta máxima o disponibilidad de los recursos limitados. 

---

## Pregunta 10
Un problema de asignación busca emparejar **m** conductores con **m** vehículos para minimizar costos. Se plantea la siguiente restricción: $\sum_{i=1}^m \sum_{j=1}^m x_{ij} = m$

¿Qué limitación tiene esta restricción?  

- [ ] No garantiza que cada vehículo reciba un conductor.
- [ ] No garantiza que cada conductor reciba un vehículo.
- [x] **No garantiza que la asignación sea uno a uno.**
- [ ] No tiene problemas, es una restricción correcta.

**Explicación:** Esa sumatoria total asegura que habrá exactamente $m$ asignaciones en general, pero no prohíbe que un vehículo reciba todos los conductores y los demás cero. Faltan las sumatorias individuales por filas y columnas ($\sum x_{ij} = 1$) que garantizan una asignación uno a uno válida.

---

## Pregunta 11
En un problema de asignación con costos variables, se quiere minimizar la función objetivo: $\sum_{i=1}^n \sum_{j=1}^n c_{ij} x_{ij}$
Donde $c_{ij}$ es el costo de asignar el recurso $i$ a la tarea $j$. Si no se incluyen restricciones adecuadas, ¿qué efecto podría tener esto en la solución del problema?  

- [ ] Se podrían obtener soluciones en las que $x_{ij}$ no sea binaria
- [ ] Se podrían asignar múltiples recursos a la misma tarea.
- [ ] Algunas tareas podrían no recibir ningún recurso.
- [x] **Todas las anteriores.**

**Explicación:** Un modelo de optimización matemática siempre buscará reducir la función objetivo sin importar la lógica. Sin definir adecuadamente el modelo base (restricciones de integralidad binaria y restricciones limitantes de filas/columnas), la solución carecerá de validez lógica cayendo en esos y otros errores.

---

## Pregunta 12
Si la oferta total excede la demanda total en un problema de transporte, ¿cómo se ajusta el modelo?  

- [ ] Se eliminan algunos orígenes para equilibrar la oferta y la demanda.
- [x] **Se agrega un destino ficticio con demanda igual al exceso de oferta.**
- [ ] Se ajustan los costos de transporte para forzar el equilibrio.
- [ ] No es posible resolver el problema si la oferta y la demanda no son iguales.

**Explicación:** Para aplicar algoritmos tradicionales del [[Problema de Transporte]] estandarizado, el modelo se balancea creando un [[Nodo ficticio]] (dummy) hacia donde la sobreoferta fluye con un costo unitario de 0.

---

## Pregunta 13
En un problema de transporte con **m** fábricas y **n** clientes, un estudiante plantea la siguiente restricción para asegurar que la demanda de cada cliente sea satisfecha: $\sum_{i=1}^m x_{ij} \le d_j, \forall j$
¿Cuál es el problema con esta formulación?  

- [x] **Permite que la demanda de algunos clientes no sea satisfecha completamente.**
- [ ] No garantiza que toda la oferta disponible en las fábricas sea utilizada.
- [ ] Permite que la demanda de algunos clientes sea superada.
- [ ] No tiene problemas, es una restricción correcta.

**Explicación:** La condición de la restricción es $\le$ (menor o igual a la demanda). Esto matemáticamente permite que la cantidad enviada al cliente $j$ sea deficiente e inferior a $d_j$. Debería ser $=$ o $\ge$ para evitar este problema.

---

## Pregunta 14
En la formulación matemática del problema de transporte, ¿qué representan las variables de decisión?  

- [ ] La demanda total de cada destino.
- [ ] Los costos unitarios de transporte en cada ruta.
- [ ] La oferta total en cada origen.
- [x] **La cantidad de bienes transportados de cada origen a cada destino.**

**Explicación:** En estos modelos matemáticos, $x_{ij}$ es una variable continua y representa el "flujo" logístico: los bienes, productos o unidades enviados desde el nodo de origen $i$ hacia el nodo de destino $j$.

---

## Pregunta 15
Si un nodo de transbordo tiene más flujo de salida que de entrada, ¿qué significa esto?  

- [ ] No afecta la solución del problema.
- [x] **Hay un error en la formulación del modelo.**
- [ ] Se ha generado un excedente de bienes en el nodo.
- [ ] Indica que el nodo tiene costos negativos de transporte.

**Explicación:** Un [[Nodo de transbordo]] puro obedece la regla inquebrantable de la [[Conservación de flujo]] (el flujo total de entrada debe igualar al flujo total de salida). Si matemáticamente hay más salida, se está "creando" material que no existe, lo cual es un error en el modelo.

---

## Pregunta 16
¿Cómo se modifica la formulación matemática de un problema de transporte para convertirlo en un problema de transbordo?  

- [ ] Se eliminan las restricciones de oferta y demanda.
- [ ] Se convierte en un problema de asignación.
- [x] **Se agregan nodos intermedios con restricciones de conservación de flujo.**
- [ ] Se usan variables binarias en lugar de continuas.

**Explicación:** El [[Problema de transbordo]] extiende el transporte clásico habilitando la existencia de nodos intermedios (que pueden no tener oferta o demanda inherente), forzando a que obedezcan la ley de conservación (Entrada - Salida = 0).

---

## Pregunta 17
¿Qué papel juegan los nodos de transbordo en la estructura de la red?  

- [x] **Permiten dividir envíos en múltiples rutas o consolidarlos antes de llegar a su destino final.**
- [ ] Reducen los costos de transporte automáticamente.
- [ ] Sirven solo para aumentar la complejidad del modelo sin impacto en la solución.
- [ ] Actúan como orígenes y destinos adicionales.

**Explicación:** Operan como "hubs" logísticos donde la carga o envíos pueden combinarse y/o reorganizarse facilitando el ruteo eficiente hacia los destinos finales.

---

## Pregunta 18
En el **Algoritmo de Sistema de Hormigas**, después de crear una ruta, la cantidad de feromonas depositadas en cada arco depende de:  

- [ ] Un valor fijo predefinido
- [x] **La calidad de la solución encontrada**
- [ ] La distancia de la ruta
- [ ] Ninguna de las anteriores

**Explicación:** En [[ACO]], una vez que las hormigas finalizan su recorrido, depositan un rastro de feromona. Dicha cantidad es inversamente proporcional al costo del recorrido; es decir, las mejores rutas (mayor calidad de la solución) reciben un mayor depósito de feromona.

---

## Pregunta 19
En un problema de Selección de Características (Feature Selection), ¿cómo se modela el espacio de búsqueda si decidimos usar el Algoritmo de Colonia de Hormigas (ACO)?  

- [ ] Como una función continua de n dimensiones donde cada eje representa la importancia de la variable.
- [ ] Como un enjambre de partículas donde cada posición es un subconjunto de datos.
- [ ] Como una colmena donde cada abeja recolecta néctar de las variables con mayor correlación.
- [x] **Como un grafo donde cada nodo es una característica y las aristas representan la transición entre elegir una variable u otra.**

**Explicación:** Para resolver un problema con [[ACO]], este debe plantearse primero como un grafo en el que las hormigas puedan "caminar". En [[Feature Selection]], se navega un grafo donde cada nodo seleccionado equivale a añadir una característica al modelo.

---

## Pregunta 20
Se tienen los siguientes padres en un algoritmo genético:
Padre 1: ABCDE
Padre 2: 12345

Después de aplicar un cruce de dos puntos se obtienen los siguientes hijos:
Hijo 1: A23DE
Hijo 2: 1BC45

**¿En qué posiciones se realizaron los puntos de corte?**  

- [ ] Después de la segunda y tercera posición
- [ ] Después de la cuarta y quinta posición
- [ ] Después de la segunda y cuarta posición
- [x] **Después de la primera y tercera posición**

**Explicación:** El [[Cruce de dos puntos]] requiere sustituir el segmento intermedio de los padres. El Hijo 1 tiene la "A" de P1 (corte tras el elemento 1), el segmento "23" de P2 (corte tras el elemento 3), y finaliza con "DE" de P1. 

---

## Pregunta 21
En un **problema de asignación** con $m$ recursos y $n$ tareas, ¿cómo se representa la matriz de costos?  

- [ ] Una matriz $m \times m$ donde las filas representan los recursos y las columnas las tareas.
- [ ] Una matriz $n \times m$ donde las filas representan las tareas y las columnas los recursos.
- [x] **Una matriz $m \times n$ donde las filas representan los recursos y las columnas las tareas, y cada celda muestra el costo de asignar el recurso $i$ a la tarea $j$.**
- [ ] Una matriz $n \times n$ donde las filas representan los recursos y las columnas las tareas.

**Explicación:** Cuando no es una asignación de tamaño simétrico, la convención del `[[Problema de asignación]]` utiliza una matriz de costos general donde las $m$ filas son orígenes/recursos y las $n$ columnas son destinos/tareas, albergando el costo $c_{ij}$.

---

## Pregunta 22
En un **problema de asignación** con $m$ recursos y $n$ tareas, ¿cómo se representaría la función objetivo si se desea minimizar el costo de asignación?  

- [x] **Minimizar la suma de los costos de asignación entre todos los recursos y todas las tareas.**
- [ ] Maximizar la cantidad de tareas asignadas.
- [ ] Minimizar el número total de recursos asignados.
- [ ] Maximizar la asignación de recursos a las tareas con menores costos.

**Explicación:** La formulación estándar de la [[Función objetivo]] es la sumatoria múltiple $\min \sum \sum c_{ij} x_{ij}$, buscando minimizar el costo global de todos los emparejamientos recurso-tarea.

---

## Pregunta 23
En un **problema de asignación** en el que se asignan recursos (trabajadores) a tareas, ¿cuál es la restricción adecuada para garantizar que cada trabajador se asigne a una única tarea?  

- [ ] La suma de todas las asignaciones de las tareas a los recursos debe ser igual a 1.
- [x] **La suma de todas las asignaciones de un trabajador a las tareas debe ser igual a 1.**
- [ ] La suma de todas las asignaciones de un trabajador a las tareas debe ser mayor o igual a 1.
- [ ] La suma de todas las asignaciones de un trabajador a las tareas debe ser menor o igual a 1.

**Explicación:** La restricción matemática para evitar superposiciones de trabajos en un mismo empleado se modela forzando la suma $\sum_j x_{ij} = 1$ para cada recurso o trabajador particular $i$.

---

## Pregunta 24
¿Qué condición debe cumplirse para que un **problema de transporte** esté equilibrado?  

- [ ] Las capacidades de los orígenes deben ser mayores que las demandas de los destinos.
- [ ] La cantidad total de productos a transportar debe ser igual a la cantidad total de productos disponibles.
- [x] **La demanda total de los destinos debe ser igual a la cantidad total de productos disponibles en los orígenes.**
- [ ] No se necesita ninguna condición para el equilibrio.

**Explicación:** Matemáticamente un [[Problema de Transporte]] está balanceado y cerrado cuando $\sum Ofertas = \sum Demandas$. Si no es así, requiere añadir un nodo dummy o ficticio para compensarlo.

---
## Pregunta 25
En el contexto de clustering, si un algoritmo ABC está buscando la posición óptima de los clusters, ¿qué sucede cuando una fuente de alimento (solución) no mejora tras muchos ciclos?  

- [ ] Se duplican las abejas en esa zona para intentar rescatar la solución.
- [ ] Se detiene el algoritmo por completo y se entrega el resultado actual.
- [ ] Se aumenta la importancia de esa solución para forzar la mejora.
- [x] **La solución se abandona y la abeja se convierte en exploradora para encontrar una posición de centroides totalmente nueva.**

**Explicación:** En el [[Algoritmo ABC]], cuando una solución se estanca y supera un límite predefinido de iteraciones (limit) sin mejorar, se abandona para prevenir caer en un mínimo local y se fomenta la exploración de nuevas áreas.

---
## Pregunta 26
Se han generado los siguientes hijos después de aplicar un operador de cruce:
Padre 1: 11011001
Padre 2: 00100110
Hijo 1:  11010110
Hijo 2:  00101001

Si el cruce ocurrió en **una única posición**, ¿en qué posición se aplicó el operador?  

- [x] **Después de la posición 4**
- [ ] Después de la posición 3
- [ ] Después de la posición 5
- [ ] Después de la posición 6

**Explicación:** Viendo el Hijo 1 (`11010110`), coincide con los primeros 4 bits del Padre 1 (`1101`) y los últimos 4 bits del Padre 2 (`0110`). Por ende, el [[Operador de cruce]] separó la cadena después de la posición 4.

---
## Pregunta 27
¿Cómo se representan matemáticamente los nodos de transbordo en un modelo de redes?  

- [ ] Como nodos de oferta con demanda cero.
- [ ] Como nodos de demanda con oferta cero.
- [ ] Como nodos que no afectan el flujo total del sistema.
- [x] **Como nodos que tienen oferta y demanda iguales.**

**Explicación:** Una forma común de representar o convertir algorítmicamente un nodo intermedio es asumiendo que su necesidad o demanda intrínseca es 0; equivalentemente, si se le asigna oferta $M$ y demanda $M$ se comportan como [[Nodos de transbordo]] al balancear su propio flujo (oferta neta = 0).

---
## Pregunta 28
Al optimizar los hiperparámetros de un modelo (como la regularización λ), el algoritmo ABC utiliza "abejas observadoras". ¿Cuál es su función crítica en este proceso?  

- [x] **Elegir y explotar las regiones del espacio de hiperparámetros que las abejas empleadas reportaron como más prometedoras.**
- [ ] Generar valores de hiperparámetros totalmente aleatorios para reiniciar el modelo.
- [ ] Calcular el gradiente de la función de pérdida para decidir la dirección del ajuste.
- [ ] Realizar un escaneo exhaustivo de todos los valores posibles de los hiperparámetros en orden secuencial.

**Explicación:** En el [[Algoritmo de Colonia Artificial de Abejas (ABC)]], las abejas "observadoras" esperan en la colmena y seleccionan las fuentes de alimento (soluciones) basándose en la información de calidad que traen las abejas "empleadas", enfocándose en intensificar la búsqueda en las mejores áreas.

---

## Pregunta 29
Dado el siguiente par de padres representados en forma binaria:
Padre 1: 10110110
Padre 2: 01001001

Si se aplica **cruce de un punto** en la **posición 4** (contando desde la izquierda y comenzando en 1), ¿cuál es la descendencia generada?  

- [ ] Hijo 1: 10110110, Hijo 2: 01001001
- [ ] Hijo 1: 10101001, Hijo 2: 01010110
- [ ] Hijo 1: 10111100, Hijo 2: 01000011
- [x] **Hijo 1: 10111001, Hijo 2: 01000110**

**Explicación:** Con el [[Cruce de un punto]], seccionamos ambas cadenas tras el 4to bit: `1011 | 0110` y `0100 | 1001`. Cruzando las partes derechas se obtiene Hijo 1 = `1011` + `1001` = `10111001` y el Hijo 2 = `0100` + `0110` = `01000110`.

---
