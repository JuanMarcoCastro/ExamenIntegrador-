# 📚 Banco de Preguntas: Tema Probabilidad Estadistica

## Pregunta 1
Dada la siguiente matriz de transición de una cadena de Markov con tres estados:

![[Pasted image 20260510181637.png]]

si el sistema inicia en el estado 2 (S_2), ¿cuál es la probabilidad de que en el siguiente paso se encuentre en el estado 3 (S_3)?

- [ ] 0.5
- [ ] 0.1
- [ ] 0.6
- [x] **0.3**

**Explicación:** En una [[Cadena de Markov]], las filas representan el estado actual y las columnas el estado siguiente. La fila 2 (Estado S_2) indica las probabilidades de transición hacia S_1, S_2 y S_3 respectivamente. El valor en la fila 2, columna 3 es `0.3`, que representa la [[Probabilidad de transición]] de ir de S_2 a S_3.

---

## Pregunta 2
Se tiene una cadena de Markov con estados (S_1,S_2,S_3). Si se sabe que el sistema está en el estado S_2 en el tiempo t, ¿cómo se calcula la probabilidad de que en el tiempo t+1 el sistema esté en el estado S_3?

- [ ] Se usa la ley de los grandes números para estimar la probabilidad empírica.
- [ ] Se debe conocer toda la historia previa de la cadena para calcular la probabilidad de transición.
- [ ] Se calcula sumando las probabilidades de transición desde todos los estados anteriores al estado S_3.
- [x] **Se obtiene directamente de la matriz de probabilidades de transición, considerando solo el estado actual S_2.**

**Explicación:** La propiedad fundamental de las [[Cadenas de Markov]] es la "falta de memoria" (propiedad de Markov), lo que significa que el estado futuro solo depende del estado actual y no de la historia pasada. Por lo tanto, basta con ver la celda correspondiente al estado actual y futuro en la matriz.

---

## Pregunta 3
En la ecuación de regresión Y=B_0+B_1X, B_1 representa:

- [ ] La variable dependiente.
- [ ] La ordenada al origen.
- [ ] La variable independiente.
- [x] **La pendiente del modelo.**

**Explicación:** En un modelo de `[[Regresión lineal simple]]`, $B_0$ es el intercepto (ordenada al origen) y $B_1$ representa la pendiente. La pendiente indica cuánto cambia en promedio la `[[Variable dependiente]]` (Y) por cada unidad de incremento en la `[[Variable independiente]]` (X).

---

## Pregunta 4
Un investigador quiere analizar la relación entre las horas de estudio y el puntaje obtenido en un examen. Decide ajustar un modelo de regresión lineal simple de la forma: Y=B_0+B_1X+e

Si X representa el número de horas de estudio e Y el puntaje en el examen, ¿cuál de las siguientes afirmaciones es correcta?

- [ ] X es la variable dependiente porque es la que se quiere predecir.
- [ ] La variable dependiente es la que tiene un coeficiente más grande en el modelo.
- [ ] Ninguna es la variable dependiente, ya que en la regresión lineal simple no hay distinción entre dependiente e independiente.
- [x] **Y es la variable dependiente porque es el resultado que se intenta explicar a partir de X.**

**Explicación:** En cualquier análisis de regresión, a la variable que buscamos estimar, predecir o explicar se le conoce como la `[[Variable dependiente]]` (comúnmente denotada como Y), que aquí es el puntaje. Las variables que usamos como predictores son las `[[Variables independientes]]` (X).

---

## Pregunta 5
Observa con atención el siguiente diagrama de dispersión, que representa un modelo de regresión lineal simple:

![[Pasted image 20260510181756.png]]

Con base en el diagrama y la ecuación del modelo, ¿cuál de las siguientes opciones representa correctamente la variable dependiente en el modelo de regresión lineal?

- [ ] La variable dependiente del modelo de regresión es B0+B1X+e
- [ ] La variable dependiente del modelo es B0+B1X
- [ ] La variable dependiente del modelo de regresión lineal es X
- [x] **La variable dependiente del modelo es Y**

**Explicación:** La `[[Variable dependiente]]` siempre es la variable respuesta que se ubica en el eje Y del gráfico de dispersión y es representada matemáticamente por la letra $Y$ en la ecuación de la regresión.

---

## Pregunta 6
En un modelo de regresión lineal múltiple, la suposición de homocedasticidad implica que:

- [ ] Los residuos tienen una distribución normal.
- [ ] Las variables independientes no están correlacionadas.
- [ ] Ninguna de las anteriores.
- [x] **Los residuos tienen una varianza constante.**

**Explicación:** La `[[Homocedasticidad]]` es un supuesto fundamental en los modelos de regresión lineal, el cual dicta que la dispersión (varianza) de los errores/residuos se mantiene constante a lo largo de todos los valores de las variables explicativas.

---

## Pregunta 7
¿Cuál es la principal razón por la que se verifica la normalidad de los residuos en un modelo de regresión lineal múltiple?

- [ ] Porque la normalidad de los residuos es necesaria para calcular el coeficiente de determinación R^2
- [ ] Porque la normalidad de los residuos garantiza que los coeficientes de regresión sean óptimos.
- [ ] Porque un modelo con residuos no normales no puede utilizarse para predecir valores futuros.
- [x] **Porque la inferencia estadística (pruebas de hipótesis e intervalos de confianza) se basa en la suposición de normalidad de los errores.**

**Explicación:** Si bien las predicciones y los coeficientes pueden calcularse sin normalidad, las pruebas estadísticas como los `[[Valores p]]` y los intervalos de confianza requieren que los residuos sigan una `[[Distribución normal]]` para que sus resultados sean válidos.

---

## Pregunta 8
¿Cuál de las siguientes opciones NO es una suposición del modelo de regresión lineal múltiple?

- [ ] Linealidad.
- [ ] Homocedasticidad.
- [ ] No multicolinealidad.
- [x] **Todas las variables independientes deben ser categóricas.**

**Explicación:** En la `[[Regresión lineal múltiple]]`, las variables independientes pueden ser de cualquier tipo (numéricas continuas, discretas o categóricas convertidas en variables dummy). No es obligatorio que sean exclusivamente categóricas.

---

## Pregunta 9
Un economista construye un modelo de regresión lineal múltiple para predecir el ingreso mensual de una persona en función de:
X1: Años de educación.
X2: Experiencia laboral en años.
X3: Género (1 si es hombre, 0 si es mujer).

Tras estimar el modelo, obtiene: Y = 2000 + 500(X1) + 300(X2) - 800(X3)

¿Cuál es la interpretación correcta del coeficiente asociado a X3 en este modelo?

- [ ] No se puede interpretar el coeficiente de X3 porque es una variable categórica.
- [ ] El coeficiente de X3 indica que los ingresos dependen únicamente del género, sin importar la educación o experiencia laboral.
- [ ] Los hombres ganan en promedio $800 más que las mujeres, manteniendo constantes los otros factores.
- [x] **Las mujeres ganan en promedio $800 más que los hombres, manteniendo constantes los otros factores.**

**Explicación:** Como la variable X3 vale 1 para hombres, el término $-800(X3)$ resta 800 al estimado del hombre. Esto significa que los hombres ganan $800 menos que las mujeres, o visto de otra forma, que las mujeres (que son la categoría de referencia con X3=0) ganan $800 más que los hombres, manteniendo el resto de las `[[Variables independientes]]` constantes.

---

## Pregunta 10
¿Cuál de los siguientes métodos se usa para detectar la presencia de multicolinealidad en un modelo de regresión lineal múltiple?

- [ ] La prueba de Durbin-Watson
- [ ] La prueba de Levene
- [ ] La prueba de Shapiro-Wilk
- [x] **El estadístico de inflación de la varianza (VIF)**

**Explicación:** El `[[Factor de Inflación de la Varianza]]` (VIF) es una métrica empleada para identificar la `[[Multicolinealidad]]`. Nos dice qué tanto se infla la varianza de un coeficiente estimado debido a la alta correlación entre las variables independientes.

---

## Pregunta 11
¿Cuál de las siguientes opciones NO es una suposición del modelo de regresión lineal múltiple?

- [ ] No multicolinealidad.
- [ ] Linealidad.
- [ ] Homocedasticidad.
- [x] **Todas las variables independientes deben ser categóricas.**

**Explicación:** *Esta pregunta es un duplicado de la Pregunta 8. El fundamento es el mismo: las variables predictoras no tienen la obligación de ser exclusivamente categóricas.*

---

## Pregunta 12
¿Qué método puedes usar para verificar la normalidad de los residuos en un análisis de regresión?

- [ ] Histograma
- [ ] Prueba de Shapiro-Wilk
- [ ] Gráfico Q-Q
- [x] **Todas las anteriores**

**Explicación:** Para validar el supuesto de `[[Distribución normal]]` en los residuos se utilizan herramientas gráficas, como el `[[Histograma]]` y el `[[Gráfico Q-Q]]`, acompañadas de pruebas formales estadísticas como la `[[Prueba de Shapiro-Wilk]]`.

---

## Pregunta 13
Un banco quiere desarrollar un modelo para predecir si una transacción es fraudulenta o no...
La variable objetivo Y toma el valor 1 si la transacción es fraudulenta y 0 si no lo es.

¿Qué tipo de regresión es más adecuada para este problema?

- [ ] Regresión lineal múltiple, porque hay varias variables predictoras.
- [ ] Regresión polinómica, porque la relación entre monto y fraude podría no ser lineal.
- [ ] Regresión de Poisson, porque se trata de un conteo de eventos fraudulentos.
- [x] **Regresión logística, porque la variable de salida es binaria (fraude/no fraude).**

**Explicación:** Para problemas de `[[Clasificación Binaria]]` (donde la `[[Variable dependiente]]` toma solo dos valores categóricos, como 0 y 1), se emplea la `[[Regresión Logística]]` porque garantiza que las predicciones se mantengan dentro del rango de probabilidades (0 a 1).

---

## Pregunta 14
Un banco quiere desarrollar un modelo que prediga si un cliente es apto (1) o no apto (0) para recibir un crédito...

¿Qué tipo de modelo es más adecuado para este problema?

- [ ] Regresión de Poisson, porque el número de clientes aprobados sigue una distribución discreta.
- [ ] Regresión de mínimos cuadrados, porque minimiza el error cuadrático medio en problemas de clasificación.
- [ ] Regresión lineal múltiple, porque varias variables explicativas influyen en la decisión del crédito.
- [x] **Regresión logística, porque la variable objetivo es binaria (apto/no apto).**

**Explicación:** Igual que en el caso del fraude, al ser una predicción de dos clases concretas ("apto" o "no apto"), el algoritmo correcto es una `[[Regresión Logística]]`.

---

## Pregunta 15
Si X y Y son variables aleatorias independientes, ¿cuál de las siguientes es verdadera?

- [ ] Cov(X,Y)=0
- [ ] E(XY)=E(X)E(Y)
- [ ] sigma^2_{X+Y}=sigma^2_X+sigma^2_Y
- [x] **Todas las anteriores**

**Explicación:** La independencia estocástica entre dos `[[Variables aleatorias]]` implica que su `[[Covarianza]]` es cero, la esperanza matemática de su producto es igual al producto de sus esperanzas, y la varianza de la suma de ambas es equivalente a la suma de sus varianzas. 

---

## Pregunta 16
Un científico quiere analizar si tres diferentes técnicas de estudio afectan el desempeño académico de los estudiantes en un examen de matemáticas. Cada técnica es aplicada a un grupo diferente de alumnos.

¿Cuál de los siguientes enfoques sería el más adecuado para analizar los datos?

- [ ] Un ANOVA de dos vías.
- [ ] Un ANOVA factorial mixto.
- [ ] Un ANOVA de medidas repetidas.
- [x] **Un ANOVA de una vía.**

**Explicación:** Dado que queremos evaluar las diferencias de medias numéricas (desempeño académico) entre 3 o más grupos separados generados por un solo factor o variable categórica (técnica de estudio), la prueba correcta es el `[[ANOVA de una vía]]` (Análisis de Varianza unidireccional).

---

## Pregunta 17
Un investigador obtiene la siguiente tabla ANOVA en regresión (SC Regresion=450, gl=2, F=5.63).
Si el nivel de significancia es 0.05, ¿qué conclusión se puede extraer?

- [ ] No hay evidencia suficiente para afirmar que la regresión es significativa.
- [ ] Todas las variables predictoras son significativas en el modelo.
- [ ] La prueba ANOVA no es aplicable a modelos de regresión.
- [x] **Se rechaza la hipótesis nula, indicando que al menos una variable predictora es significativa.**

**Explicación:** En el marco de la regresión, la tabla `[[ANOVA]]` realiza una "prueba F de significancia global". Un valor de F estadísticamente significativo (es decir, p-valor < 0.05) nos lleva a rechazar la `[[Hipótesis nula]]` que afirma que todos los coeficientes de regresión son cero. Concluyendo que el modelo en conjunto sí predice los datos (al menos un B_i es diferente de cero).

---

## Pregunta 18
Un investigador analiza si existe diferencia en el rendimiento académico de estudiantes según el método de enseñanza. Obtiene tabla ANOVA con F=5.32 y p-valor=0.008.

- [ ] El valor de F es 5.32, lo que indica que los tres métodos tienen el mismo efecto en el rendimiento académico.
- [ ] No se puede sacar ninguna conclusión sin conocer la media y desviación estándar de cada grupo.
- [ ] Como la SC entre grupos es menor que la SC dentro de grupos, significa que no hay diferencias significativas.
- [x] **Dado que el p-valor (0.008) es menor a 0.05, podemos rechazar la hipótesis nula y concluir que al menos un grupo tiene una media diferente.**

**Explicación:** El `[[Valor p]]` es el indicador más directo para tomar una decisión en las pruebas de hipótesis. Puesto que 0.008 < 0.05 (nivel de significancia estándar), se rechaza la `[[Hipótesis nula]]`, probando con significancia estadística que los grupos analizados en el `[[ANOVA]]` no tienen medias idénticas.

---

## Pregunta 19
En un estudio sobre factores de estrés laboral, un analista de datos utiliza un modelo de ecuaciones estructurales (SEM) para evaluar la relación entre variables latentes... La tabla ANOVA se emplea para:

- [ ] Comprobar si la relación entre las variables latentes sigue una distribución normal.
- [ ] Evaluar si los coeficientes de regresión de las variables latentes son significativos.
- [ ] Medir la correlación entre los factores de estrés y la satisfacción laboral.
- [x] **Determinar si los diferentes grupos de empleados muestran diferencias significativas en los valores esperados de las variables latentes.**

**Explicación:** La función nativa y fundamental del Análisis de Varianza o `[[ANOVA]]` es identificar si existen diferencias estadísticamente significativas en las medias observadas al separar y agrupar los datos en distintas categorías (por ejemplo, comparar grupos de empleados bajo diferentes condiciones).

---

## Pregunta 20
Se sabe que la distribución marginal g(y)=1/3, 0<y<3. Además, la distribución condicional f(x|y) = (x+y)/6, 0<x<2.
¿Cuál de las siguientes expresiones corresponde a la función de densidad conjunta?

- [ ] f(x,y) = (x+y)/6
- [ ] f(x,y) = (x+y)/3
- [ ] f(x,y) = (x+y)/12
- [x] **f(x,y) = (x+y)/18 , 0<x<2, 0<y<3**

**Explicación:** Por definición de `[[Probabilidad Condicional]]`, la función de `[[Densidad Conjunta]]` $f(x,y)$ se obtiene multiplicando la `[[Distribución Marginal]]` por la `[[Distribución Condicional]]`.  
$f(x,y) = f(x|y) \times g(y)$  
$f(x,y) = \frac{x+y}{6} \times \frac{1}{3} = \frac{x+y}{18}$

---

## Pregunta 21
Un restaurante tiene dos niveles de ocupación: **baja** y **alta**. Se observa que si hoy la ocupación es **baja**, la probabilidad de que mañana también sea **baja** es de **0.7**. Si hoy la ocupación es **alta**, la probabilidad de que mañana siga siendo **alta** es de **0.5**. 

Definimos los estados como:
* **0**: Ocupación baja  
* **1**: Ocupación alta

Con esta información:
1. **¿Este proceso cumple con la propiedad markoviana?**  
2. **Sólo si su respuesta es afirmativa, ¿Cuál es la matriz de transición correspondiente?**

- [ ] No cumple con la propiedad markoviana porque la ocupación de un día depende de más de un solo día anterior.
- [ ] **Sí cumple con la propiedad markoviana.** Su matriz de transición es: [0.7 0.5 ; 0.3 0.5]
- [x] **Sí cumple con la propiedad markoviana.** Su matriz de transición es: [0.7 0.3 ; 0.5 0.5]
- [ ] **Sí cumple con la propiedad markoviana.** Su matriz de transición es: [0.5 0.5 ; 0.3 0.7]

**Explicación:** El proceso sí cumple la `[[Propiedad de Markov]]` porque la ocupación de mañana depende *únicamente* de la ocupación de hoy. Las probabilidades desde el estado 0 (baja) deben sumar 1: si P(0->0) = 0.7, entonces P(0->1) = 0.3. Las probabilidades desde el estado 1 (alta) también deben sumar 1: si P(1->1) = 0.5, entonces P(1->0) = 0.5. Esto genera una `[[Matriz de transición]]` con las filas `[0.7, 0.3]` y `[0.5, 0.5]`.

---

## Pregunta 22
Un economista está estudiando cómo el precio del petróleo ($ por barril) afecta el costo del transporte aéreo ($ por boleto). Decide ajustar un modelo de **regresión lineal simple** con la ecuación:

Costo del boleto = B_0 + B_1(Precio del petróleo) + e

¿Cuál de las siguientes afirmaciones es correcta sobre la variable dependiente en este modelo?

- [ ] El precio del petróleo es la variable dependiente porque afecta el costo del boleto.
- [ ] Ambas variables son dependientes, ya que el precio del petróleo y el costo del boleto están correlacionados.
- [x] **El costo del boleto es la variable dependiente porque es el resultado que se intenta predecir con el modelo.**
- [ ] No se puede determinar cuál es la variable dependiente sin más información.

**Explicación:** En una `[[Regresión lineal simple]]`, la variable que está despejada del lado izquierdo de la ecuación es la `[[Variable dependiente]]` (Y), la cual se intenta explicar o predecir en función de la `[[Variable independiente]]` (X, en este caso el precio del petróleo).

---

## Pregunta 23
¿Cuál de las siguientes afirmaciones describe correctamente el supuesto de no multicolinealidad en un modelo de regresión lineal múltiple?

- [ ] La multicolinealidad se corrige eliminando automáticamente las variables menos significativas del modelo.
- [ ] Las variables independientes deben estar altamente correlacionadas entre sí para mejorar la precisión del modelo.
- [ ] La multicolinealidad solo es un problema cuando hay más de tres variables predictoras en el modelo.
- [x] **No debe existir una relación lineal fuerte entre las variables independientes del modelo.**

**Explicación:** El supuesto de no `[[Multicolinealidad]]` en la `[[Regresión lineal múltiple]]` exige que las `[[Variables independientes]]` no estén altamente correlacionadas entre sí, ya que esto dificultaría determinar el efecto individual de cada variable sobre la variable dependiente y aumentaría la varianza de los coeficientes.

---

## Pregunta 24
¿Cuál es el propósito de realizar un análisis de regresión múltiple?

- [ ] Examinar la relación entre dos variables.
- [ ] Ninguna de las anteriores.
- [x] **Predecir la variable dependiente en función de varias variables independientes.**
- [ ] Calcular la media de una variable.

**Explicación:** La `[[Regresión lineal múltiple]]` tiene como propósito principal modelar y predecir el comportamiento de una única `[[Variable dependiente]]` continua a partir del efecto combinado de dos o más `[[Variables independientes]]`.

---

## Pregunta 25
¿Cuál de los siguientes es un supuesto de la regresión logística?

- [ ] Los datos deben tener homocedasticidad.
- [ ] Los errores están normalmente distribuidos.
- [ ] Existe una relación lineal entre las variables independientes y la variable dependiente.
- [x] **La variable dependiente es categórica y binaria.**

**Explicación:** A diferencia de la regresión lineal, la `[[Regresión Logística]]` relaja los supuestos de normalidad de residuos y linealidad directa con Y. Su supuesto y característica fundamental es que la `[[Variable dependiente]]` debe ser dicotómica/binaria (por ejemplo, éxito/fracaso, 1/0).

---

## Pregunta 26
Si Var(X+Y) = Var(X) + Var(Y), ¿qué podemos inferir acerca de las variables X e Y?

- [x] **Son independientes.**
- [ ] Tienen la misma varianza.
- [ ] Ninguna de las anteriores.
- [ ] Están correlacionadas.

**Explicación:** La fórmula general es $Var(X+Y) = Var(X) + Var(Y) + 2Cov(X,Y)$. Para que la igualdad dada se cumpla, la `[[Covarianza]]` $Cov(X,Y)$ debe ser igual a 0. Aunque técnicamente esto solo implica que están incorrelacionadas, en el contexto estándar de probabilidad básica esto suele ser la propiedad clave que se asume e infiere cuando las `[[Variables aleatorias]]` son independientes.

---

## Pregunta 27
Un biólogo investiga si diferentes fertilizantes afectan el crecimiento de las plantas. Los datos obtenidos se resumen en la siguiente tabla ANOVA:

| Fuente de Variación | Suma de Cuadrados (SC) | Grados de Libertad (GL) | Cuadrados Medios (CM) | Valor F | p-valor |
| ----- | ----- | ----- | ----- | ----- | ----- |
| Entre grupos | 320.5 | 3 | 106.83 | 7.91 | 0.001 |
| Dentro de grupos | 980.3 | 46 | 21.31 |  |  |
| Total | 1300.8 | 49 |  |  |  |

¿Qué componente de la tabla permite determinar si los fertilizantes tienen un efecto significativo en el crecimiento de las plantas?

- [ ] El cuadrado medio dentro de los grupos (CM = 21.31).
- [x] **El valor F (7.91) y el p-valor (0.001), porque permiten determinar si la diferencia entre grupos es estadísticamente significativa.**
- [ ] La suma de cuadrados total (SC = 1300.8).
- [ ] El grado de libertad dentro de grupos (GL = 46).

**Explicación:** En una tabla `[[ANOVA]]`, el estadístico de prueba es el Valor F, y la decisión sobre si existen diferencias significativas reales se toma observando el `[[Valor p]]` asociado. Un p-valor pequeño (menor que el nivel de significancia) indica que los grupos sí tienen medias diferentes.

---

## Pregunta 28
Un investigador educativo quiere analizar si existen diferencias significativas en las calificaciones promedio de estudiantes de tres colegios diferentes (A, B y C). Para ello, selecciona una muestra de estudiantes de cada colegio y aplica un ANOVA de una vía.

¿Cuáles son la hipótesis nula y la hipótesis alternativa en este estudio?

- [ ] H_0: La varianza de las calificaciones es la misma... H_1: La varianza es diferente...
- [x] **H_0: Todos los colegios tienen la misma media de calificaciones. H_1: Al menos un colegio tiene una media de calificaciones diferente a los demás.**
- [ ] H_0: No hay relación entre el colegio... H_1: La calificación depende del colegio...
- [ ] H_0: La media de calificaciones del Colegio A es mayor... H_1: La media del Colegio B es menor...

**Explicación:** El objetivo del `[[ANOVA de una vía]]` es comparar medias. Por definición, la `[[Hipótesis nula]]` postula que no hay diferencias (todas las medias poblacionales son iguales, $\mu_A = \mu_B = \mu_C$), mientras que la `[[Hipótesis alternativa]]` establece que al menos una media grupal difiere de las demás.

---

## Pregunta 29
Un investigador quiere analizar si existen diferencias significativas en el rendimiento académico de tres grupos de estudiantes que recibieron distintos métodos de enseñanza: presencial, en línea y mixto. Para ello, recopila las calificaciones finales de los estudiantes y aplica un ANOVA de una vía.

¿Cuál es el objetivo principal de la tabla ANOVA en este contexto?

- [ ] Comprobar si los datos cumplen con los supuestos de normalidad y homocedasticidad.
- [ ] Determinar si la varianza total de las calificaciones es mayor en algunos grupos que en otros.
- [ ] Estimar el efecto del método de enseñanza en la distribución normal de las calificaciones.
- [x] **Evaluar si la media de al menos un grupo es significativamente diferente de las demás.**

**Explicación:** El [[ANOVA]] (Análisis de Varianza) a pesar de su nombre, se utiliza primordialmente para comparar si las medias numéricas de tres o más grupos difieren estadísticamente entre sí.

---## Pregunta 30
En un **problema de asignación** donde se asignan vehículos a rutas de distribución, pero las rutas tienen capacidades limitadas (es decir, no todos los vehículos pueden cubrir todas las rutas debido a restricciones de capacidad), ¿cuál sería la restricción adecuada para modelar estas limitaciones de capacidad?  

- [ ] La suma de las asignaciones de vehículos a las rutas debe ser menor o igual a la capacidad total de vehículos disponibles.
- [ ] La suma de las asignaciones de vehículos a cada ruta debe ser igual a la cantidad total de vehículos disponibles.
- [ ] La suma de las asignaciones de vehículos a una ruta debe ser igual a la capacidad máxima de vehículos que puede cubrir esa ruta.
- [x] **La suma de las asignaciones de vehículos a una ruta debe ser menor o igual a la capacidad máxima de vehículos que puede cubrir esa ruta.**

**Explicación:** Para modelar que una ruta $j$ no se sobrecargue, se exige matemáticamente que la sumatoria de los vehículos $i$ en dicha ruta ($\sum_i x_{ij}$) sea menor o igual al límite (capacidad máxima) de esa ruta.

---

## Pregunta 31
Si usamos PSO para encontrar los mejores pesos de una regresión donde la función de error tiene muchos valles falsos, ¿qué papel juega el parámetro de "inercia" (w)?  

- [ ] Es el valor constante que se le suma al error final para normalizarlo.
- [x] **Controla el equilibrio entre explorar nuevas áreas del error y refinar la búsqueda en la zona actual.**
- [ ] Determina qué tan rápido se actualiza la base de datos de entrenamiento.
- [ ] Representa la resistencia de los datos a ser clasificados correctamente.

**Explicación:** El parámetro de inercia (`w`) en `[[PSO]]` define cuánto de la velocidad anterior se conserva, logrando un balance entre la exploración global de nuevas regiones (valores altos de w) y la explotación local (valores bajos de w).

---

## Pregunta 32
¿Cuál de los siguientes problemas puede modelarse como un problema de transbordo?  

- [ ] Determinación de la ruta más corta entre dos ciudades.
- [ ] Asignación de empleados a diferentes turnos de trabajo.
- [ ] Programación de la producción en una planta de manufactura.
- [x] **Distribución de productos desde fábricas a centros de distribución antes de llegar a tiendas.**

**Explicación:** Los "centros de distribución" son el caso de uso por excelencia de los `[[Nodos de transbordo]]`, ya que ni originan ni demandan bienes de manera terminal, sino que consolidan y enrutan mercancía entre los orígenes y las tiendas finales.

---
## Pregunta 33
¿Cuál de las siguientes afirmaciones sobre la **varianza** es **correcta**?  

- [ ] La varianza siempre tiene las mismas unidades que los datos originales.
- [x] **Si la varianza es cero, todos los valores en el conjunto de datos son iguales.**
- [ ] La varianza mide la tendencia central de los datos.
- [ ] La varianza puede tomar valores negativos si los datos están sesgados.

**Explicación:** La `[[Varianza]]` mide la dispersión cuadrática de los datos respecto a su media. Si es exactamente 0, significa que no hay dispersión y todos los puntos de datos son idénticos.

---

## Pregunta 34
¿Cuál de las siguientes no es una medida de dispersión?  

- [ ] Desviación estándar.
- [ ] Rango intercuartílico.
- [ ] Varianza.
- [x] **Moda.**

**Explicación:** La `[[Moda]]` es una `[[Medida de tendencia central]]` (indica el valor más frecuente), mientras que la varianza, desviación estándar y rango intercuartílico son medidas de dispersión estadística.

---

## Pregunta 35
¿Cuál de los siguientes conjuntos de medidas de dispersión se ve más afectado por valores atípicos en un conjunto de datos?  

- [ ] El rango intercuartílico y la mediana.
- [ ] La moda y el rango intercuartílico.
- [x] **La varianza y la desviación estándar.**
- [ ] La mediana y la desviación media absoluta.

**Explicación:** Al ser derivadas del cuadrado de las diferencias entre cada dato y la media, la `[[Varianza]]` y la `[[Desviación estándar]]` amplifican exponencialmente el impacto numérico de los `[[Valores atípicos (Outliers)]]`.

---

## Pregunta 36
Si se añade un **valor extremo muy alto** a un conjunto de datos, ¿qué medida de tendencia central se verá más afectada?  

- [x] **La media**
- [ ] La moda
- [ ] La mediana
- [ ] Ninguna, ya que todas son resistentes a valores extremos

**Explicación:** La `[[Media aritmética]]` considera la magnitud cuantitativa de todos los datos en su cálculo. Un valor excesivamente grande empujará el promedio aritmético significativamente hacia ese extremo.

---

## Pregunta 37
¿Cuál de las siguientes **afirmaciones sobre el rango intercuartílico (IQR)** es **verdadera**?  

- [x] **El IQR mide la diferencia entre el primer y tercer cuartil, abarcando el 50% central de los datos.**
- [ ] Un IQR de cero significa que la distribución es simétrica.
- [ ] Si el IQR es pequeño, significa que la media también es pequeña.
- [ ] El IQR se ve muy afectado por valores atípicos extremos.

**Explicación:** El `[[Rango Intercuartílico (IQR)]]` se calcula como $Q3 - Q1$, eliminando el 25% superior y el 25% inferior, por lo que describe exactamente la dispersión del 50% central de los datos y es robusto ante atípicos.

---

## Pregunta 38
¿Qué indica el valor p en una prueba de hipótesis?  

- [ ] El valor más probable del parámetro poblacional.
- [ ] La probabilidad de que la hipótesis nula sea verdadera.
- [x] **La probabilidad de observar un estadístico al menos tan extremo como el observado, asumiendo que la hipótesis nula es verdadera.**
- [ ] La probabilidad de que la hipótesis alternativa sea verdadera.

**Explicación:** En la `[[Inferencia estadística]]`, el `[[Valor p]]` o p-valor es una medida probabilística de la evidencia contra la hipótesis nula ($H_0$). Si es bajo, sugiere que los datos observados son muy inusuales si $H_0$ fuera correcta.

---

## Pregunta 39
¿Qué tipo de prueba estadística es más adecuada para analizar la relación entre dos variables categóricas?  

- [ ] Prueba t de Student.
- [ ] Análisis de varianza (ANOVA).
- [x] **Prueba de chi-cuadrado.**
- [ ] Regresión lineal.

**Explicación:** La `[[Prueba Chi-Cuadrado]]` de independencia es el test por excelencia para determinar si existe una asociación estadísticamente significativa entre dos variables categóricas o cualitativas.

---

## Pregunta 40
¿Cuál de las siguientes afirmaciones es verdadera acerca de los intervalos de confianza?  

- [x] **Un intervalo de confianza del 95% significa que el parámetro poblacional está dentro del intervalo en el 95% de las muestras.**
- [ ] Un intervalo de confianza siempre incluye la media de la población.
- [ ] Un intervalo de confianza más amplio indica mayor precisión en la estimación.
- [ ] Un intervalo de confianza se usa para estimar parámetros de la muestra, no de la población.

**Explicación:** La interpretación frecuentista de un `[[Intervalo de confianza]]` del 95% señala que si se extrajeran múltiples muestras aleatorias bajo las mismas condiciones y se calcularan intervalos para todas, alrededor del 95% de esos intervalos contendrían el verdadero parámetro de la población.

---

## Pregunta 41
¿Qué significa un **p-valor** de 0.03 en una prueba de hipótesis?  

- [ ] Que la hipótesis alternativa debe ser aceptada sin ninguna duda.
- [x] **Que si la hipótesis nula fuera cierta, la probabilidad de obtener un resultado tan extremo como el observado sería del 3%.**
- [ ] Que la hipótesis nula es verdadera con un 97% de confianza.
- [ ] Que hay un 3% de probabilidad de que la hipótesis alternativa sea verdadera.

**Explicación:** Un `[[Valor p]]` del 0.03 (3%) es la probabilidad condicional de obtener la misma estadística observada asumiendo ciegamente que la hipótesis nula es cierta. Generalmente, un valor menor a 0.05 es suficiente para rechazar $H_0$.

---

## Pregunta 42
¿Qué tipo de gráfico es más adecuado para visualizar la distribución de una variable cuantitativa?  

- [ ] Gráfico de barras
- [x] **Histograma**
- [ ] Diagrama de dispersión
- [ ] Diagramas de caja

**Explicación:** El `[[Histograma]]` agrupa los datos cuantitativos continuos en rangos (bins) continuos y muestra su frecuencia, revelando instantáneamente la forma, la simetría y la distribución (ej. Normal, sesgada) de los datos.

---

## Pregunta 43
¿Cuál es el objetivo principal de la inferencia estadística?  

- [ ] Normalizar los datos
- [x] **Extraer conclusiones sobre una población a partir de una muestra**
- [ ] Describir un conjunto de datos
- [ ] Eliminar el ruido en los datos

**Explicación:** A diferencia de la estadística descriptiva, la `[[Inferencia estadística]]` utiliza las matemáticas y el muestreo aleatorio para estimar y generalizar propiedades de una `[[Población]]` entera utilizando solo una fracción de los datos (`[[Muestra]]`).

---

## Pregunta 44
Dado el siguiente DataFrame:
`df = pd.DataFrame({'Nombre': ['Ana', 'Luis', 'Carlos', 'Sofia'], 'Edad': [25, 30, 35, 28]})`

¿Qué expresión devuelve solo las filas donde la edad es mayor a 28?  

- [ ] `df.loc[df['Edad'] < 28]`
- [ ] `df.loc[df['Edad'] >= 28]`
- [x] **`df.query("Edad > 28")`**
- [ ] `df.query(Edad > 28)`

**Explicación:** En `[[Pandas]]`, `.query()` acepta una cadena o string con una condición booleana para filtrar el `[[DataFrame]]` fácilmente.

---

## Pregunta 45
Tienes los siguientes DataFrames:
`df1 = pd.DataFrame({'ID': [1, 2, 3], 'Nombre': ['Ana', 'Luis', 'Carlos']})`
`df2 = pd.DataFrame({'ID': [2, 3, 4], 'Edad': [25, 30, 35]})`

¿Qué método de combinación de DataFrames devuelve un resultado que conserva **solo las filas con IDs presentes en ambos DataFrames**?  

- [ ] `df1.merge(df2, on='ID', how='right')`
- [x] **`df1.merge(df2, on='ID', how='inner')`**
- [ ] `df1.merge(df2, on='ID', how='left')`
- [ ] `df1.merge(df2, on='ID', how='outer')`

**Explicación:** En las uniones relacionales (`[[Joins (Bases de datos)]]`), el operador `inner` cruza y devuelve exclusivamente los registros cuya clave primaria de emparejamiento ('ID' en este caso) existan simultáneamente en ambas tablas.

---

## Pregunta 46
En ciencia de datos ¿Qué se entiende por transformación de datos?  

- [x] **Aplicar técnicas como escalado, normalización o logaritmos**
- [ ] Cambiar la estructura del conjunto de datos
- [ ] Eliminar variables no significativas
- [ ] Convertir datos cualitativos en cuantitativos

**Explicación:** La `[[Transformación de datos]]` en Machine Learning típicamente se refiere a procesos matemáticos y estadísticos (como `[[Normalización]]` o `[[Estandarización]]`) que ajustan la escala y distribución de las variables para optimizar los algoritmos predictivos.

---

## Pregunta 47
¿Qué información clave proporciona un **gráfico de dispersión** en un análisis estadístico?  

- [ ] La distribución de una variable categórica.
- [ ] La correlación exacta entre dos variables.
- [ ] La varianza de una única variable.
- [x] **La relación entre dos variables cuantitativas.**

**Explicación:** El `[[Diagrama de dispersión]]` o Scatter plot mapea dos variables continuas numéricas en los ejes X e Y. Esto permite identificar visualmente la relación, tendencia (lineal o no lineal), agrupaciones y presencia de outliers entre ambas.

---

## Pregunta 48
En un **gráfico de cajas y bigotes (boxplot)**, ¿qué indica la longitud de los bigotes?  

- [x] **La dispersión de los datos dentro de 1.5 veces el rango intercuartílico (IQR).**
- [ ] La cantidad de datos en el conjunto.
- [ ] El valor exacto de la media.
- [ ] La correlación entre dos variables.

**Explicación:** Por convención de John Tukey, los bigotes de un `[[Boxplot]]` se extienden desde el extremo de la caja (los cuartiles 1 y 3) hasta abarcar el valor más extremo disponible que se encuentre a una distancia matemática no mayor a $1.5 \times IQR$. Los datos fuera de este rango se marcan como valores atípicos.

---

## Pregunta 49
¿Qué método se puede usar para determinar los valores óptimos de "p" y "q" en un modelo ARIMA?  

- [ ] Test de normalidad
- [ ] Regresión logística
- [x] **Autocorrelación y autocorrelación parcial**
- [ ] Método del codo

**Explicación:** En el ajuste del modelo estadístico `[[ARIMA]]` (p,d,q), se examinan las funciones de `[[Autocorrelación (ACF)]]` y la `[[Autocorrelación parcial (PACF)]]`. La ACF ayuda a inferir "q" (componente de Media Móvil o MA), y la PACF determina "p" (componente Autorregresivo o AR).

---

## Pregunta 50
¿Qué medida de tendencia central es más sensible a los valores atípicos en un conjunto de datos?  

- [ ] Rango.
- [x] **Media.**
- [ ] Moda.
- [ ] Mediana.

**Explicación:** La `[[Media aritmética]]` es extremadamente sensible a `[[Valores atípicos (Outliers)]]`, ya que incluye todos y cada uno de los valores en su sumatoria. Un solo valor extremo puede desplazarla artificialmente hacia la derecha o izquierda.

---

## Pregunta 51
Si la media de un conjunto de datos es 50 y la mediana es 40, ¿cómo está sesgada la distribución?  

- [ ] No hay sesgo.
- [x] **Sesgo a la derecha.**
- [ ] Sesgo a la izquierda.
- [ ] No se puede determinar.

**Explicación:** Cuando la `[[Media aritmética]]` es mayor que la `[[Mediana]]`, significa que existen valores atípicamente altos que están "jalando" el promedio aritmético hacia valores positivos, lo que genera un `[[Sesgo a la derecha (Asimetría positiva)]]`.

---

## Pregunta 52
Un investigador quiere determinar si el tiempo promedio que tardan los clientes en una tienda ha cambiado con respecto al año pasado. ¿Cuál de las siguientes pruebas de hipótesis sería la más adecuada para este caso?  

- [ ] Prueba de chi-cuadrado de independencia.
- [x] **Prueba t para una muestra.**
- [ ] Prueba ANOVA.
- [ ] Prueba t para muestras independientes.

**Explicación:** Al comparar la media de una muestra actual contra un estándar histórico conocido ("el promedio del año pasado"), la metodología estadísticamente correcta es una `[[Prueba T de Student]]` para una sola muestra (One-Sample T-Test).

---

## Pregunta 53
En una prueba t de Student para dos muestras independientes, ¿cuál es el propósito de esta prueba?  

- [x] **Comparar las medias de dos muestras independientes para determinar si son significativamente diferentes.**
- [ ] Comparar la media de una muestra con una media conocida de la población.
- [ ] Comparar las medias de dos muestras dependientes.
- [ ] Comparar la mediana de dos muestras para determinar la igualdad de distribuciones.

**Explicación:** La `[[Prueba T de Student para muestras independientes]]` se diseña específicamente para evaluar si las `[[Media aritmética|Medias]]` poblacionales de dos grupos mutuamente excluyentes y no relacionados difieren de forma estadísticamente significativa.

---

## Pregunta 54
¿Cuál de los siguientes es un error de tipo I en una prueba de hipótesis?  

- [ ] No rechazar la hipótesis nula cuando es falsa.
- [x] **Rechazar la hipótesis nula cuando es verdadera.**
- [ ] Aceptar la hipótesis nula cuando es falsa.
- [ ] No rechazar la hipótesis alternativa cuando es verdadera.

**Explicación:** En la `[[Inferencia estadística]]`, el `[[Error de Tipo I]]` (Falso Positivo) ocurre al descartar la $H_0$ a pesar de que ésta era la correcta en la realidad. Equivale a detectar un efecto estadístico donde realmente no lo hay.

---

## Pregunta 55
Si realizas una prueba de hipótesis con un nivel de significancia $\alpha=0.05$, ¿qué significa esto?  

- [ ] Existe un chance del 95% de aceptar la hipótesis nula.
- [ ] Existe un chance del 5% de que la hipótesis alternativa sea falsa.
- [ ] Existe un chance del 95% de que la hipótesis nula sea verdadera.
- [x] **Existe un chance del 5% de rechazar incorrectamente la hipótesis nula cuando es verdadera.**

**Explicación:** El `[[Nivel de significancia (Alfa)]]` define exactamente la probabilidad máxima permitida de cometer un `[[Error de Tipo I]]`. Un $\alpha=0.05$ establece que toleraremos un 5% de probabilidad de rechazar una hipótesis nula cierta (falso positivo).

---

## Pregunta 56
¿Qué prueba estadística se usa para comparar las medias de dos grupos independientes?  

- [ ] ANOVA
- [x] **Prueba t de Student**
- [ ] Chi-cuadrado
- [ ] Regresión lineal

**Explicación:** Como se vio previamente, la `[[Prueba T de Student]]` es el método paramétrico estándar para evaluar la diferencia de medias entre dos, y solo dos, grupos no correlacionados.

---

## Pregunta 57
¿Cuál de las siguientes medidas NO es una medida de dispersión?  

- [ ] Varianza
- [x] **Media**
- [ ] Rango
- [ ] Desviación estándar

**Explicación:** La `[[Media aritmética]]` es una `[[Medida de tendencia central]]`, diseñada para hallar el punto de equilibrio o centro de la distribución. La varianza, el rango y la desviación estándar sí miden la separación o dispersión numérica de los datos.

---

## Pregunta 58
Dado el siguiente código:
`df1 = pd.DataFrame({'Nombre': ['Ana', 'Luis', 'Carlos']}, index=[1, 2, 3])`
`df2 = pd.DataFrame({'Edad': [25, 30, 35]}, index=[2, 3, 4])`

¿Cuál de las siguientes opciones es correcta para unir `df1` y `df2` usando los índices?  

- [ ] `df1.join(df2, how='right', on='ID')`
- [ ] `df1.join(df2, on='ID')`
- [ ] `df1.join(df2, how='outer', on='Nombre')`
- [x] **`df1.join(df2, how='inner')`**

**Explicación:** En `[[Pandas]]`, el método `.join()` por defecto combina DataFrames alineando sus `[[Índices (Bases de datos)]]`. Con `how='inner'` se retornará únicamente la intersección (en este caso, los índices 2 y 3 que existen en ambos).

---

## Pregunta 59
¿Qué técnica se usa comúnmente para manejar valores faltantes en un conjunto de datos?  

- [ ] Eliminación de registros
- [x] **Todas las anteriores**
- [ ] Imputación con la media
- [ ] Uso de modelos predictivos

**Explicación:** En el proceso de `[[Limpieza de datos]]`, el manejo de valores nulos o `[[Valores faltantes (Missing values)]]` puede abordarse matemáticamente rellenando (imputando) con estadísticas simples o complejas (medias, modelos), o directamente borrando las observaciones problemáticas.

---

## Pregunta 60
¿Qué gráfica se utiliza para identificar valores atípicos y la distribución general de un conjunto de datos?  

- [x] **Diagrama de caja.**
- [ ] Gráfico de líneas.
- [ ] Diagrama de Pareto.
- [ ] Diagrama de barras.

**Explicación:** El `[[Diagrama de caja (Boxplot)]]` resume maravillosamente la distribución en cuartiles, la asimetría, y además representa visualmente los valores individuales atípicos como puntos externos a sus "bigotes".

---

## Pregunta 61
¿Cuál de los siguientes gráficos se utiliza comúnmente para evaluar la relación entre los valores observados y los valores predichos en la regresión lineal?  

- [x] **Diagrama de dispersión.**
- [ ] Gráfico de barras.
- [ ] Histograma.
- [ ] Diagrama de cajas.

**Explicación:** En un análisis de predicción (`[[Regresión lineal]]`), situamos los valores reales observados en el eje Y y los predichos en el eje X dentro de un `[[Diagrama de dispersión]]` para observar gráficamente qué tan cerca están de la línea identidad perfecta.

---

## Pregunta 62
¿Qué gráfico es ideal para detectar valores atípicos en un conjunto de datos?  

- [ ] Gráfico de pastel
- [ ] Gráfico de radar
- [ ] Gráfico de líneas
- [x] **Boxplot**

**Explicación:** Esta es otra forma de validar la utilidad del `[[Boxplot]]`. Al trazar un límite analítico (generalmente de $1.5 \times IQR$), identifica de manera automática e imparcial a los datos extremos u outliers.

---

## Pregunta 63
¿Qué hace la función de autocorrelación parcial (PACF) en el análisis de series de tiempo?  

- [x] **Mide la dependencia de un punto con su pasado después de eliminar efectos intermedios**
- [ ] Identifica patrones de tendencia
- [ ] Indica si la serie es estacionaria
- [ ] Predice valores futuros

**Explicación:** A diferencia de la ACF normal, la `[[Autocorrelación parcial (PACF)]]` aísla la relación estadística directa (o de "puro efecto") entre un dato en el tiempo $t$ y un valor pasado $t-k$, retirando la influencia de todos los periodos que existieron en el medio de ellos.

---

## Pregunta 64
¿Cuál de los siguientes enunciados describe mejor la interpretación de los números de Betti?  

- [ ] La media, varianza y asimetría estadística de los conjuntos de datos
- [ ] Las diferentes medias de nuestros datos
- [x] **El número de componentes conexas, lazos y hoyos en el espacio**
- [ ] El número total de vértices en una representación gráfica de los datos

**Explicación:** Los `[[Números de Betti]]` son invariantes topológicos que cuantifican las características de un espacio: $b_0$ cuenta las componentes conexas, $b_1$ los agujeros o túneles circulares bidimensionales, y $b_2$ las cavidades o vacíos tridimensionales.

---

## Pregunta 65
Si el **coeficiente de asimetría** de una distribución es **negativo**, ¿qué significa esto?  

- [x] **Que la distribución tiene una cola más larga hacia la izquierda.**
- [ ] Que la moda es mayor que la media y la mediana.
- [ ] Que la distribución es simétrica.
- [ ] Que la mediana es mayor que la moda, pero menor que la media.

**Explicación:** Un coeficiente de `[[Asimetría (Skewness)]]` negativo o sesgo a la izquierda ocurre cuando hay algunos valores atípicamente pequeños que alargan la cola del lado izquierdo de la distribución, jalando la media hacia valores inferiores.

---

## Pregunta 66
Dado el siguiente DataFrame:
`df = pd.DataFrame({'Categoria': ['A', 'B', 'A', 'B', 'A'], 'Valor': [10, 20, 30, 40, 50]})`

¿Qué operación devolvería la **suma de "Valor" para cada "Categoria"**?  

- [ ] `df.groupby('Valor')['Categoria'].sum()`
- [ ] `df.groupby('Categoria')['Valor'].count()`
- [ ] `df.groupby('Categoria').sum()`
- [x] **`df.groupby('Categoria')['Valor'].sum()`**

**Explicación:** En `[[Pandas]]`, la agregación se realiza usando `.groupby()`. Al agrupar por la columna `'Categoria'`, luego seleccionamos específicamente la columna a sumar (`['Valor']`) y aplicamos la función de reducción `.sum()`.

---

## Pregunta 67
En un diagrama de dispersión, ¿qué indica la presencia de una nube de puntos con una clara tendencia ascendente?  

- [ ] Una distribución normal
- [x] **Una correlación positiva**
- [ ] Una correlación negativa
- [ ] No hay relación entre las variables

**Explicación:** Al analizar un `[[Diagrama de dispersión]]`, una tendencia ascendente (de abajo izquierda a arriba derecha) visualiza que a medida que aumenta la variable X, también lo hace la variable Y, lo que define numéricamente una `[[Correlación de Pearson|Correlación positiva]]`.

---
## Pregunta 68
¿Cuál es la principal ventaja de utilizar un enfoque bayesiano en el modelado estadístico?  

- [ ] Siempre proporciona resultados exactos sin importar los datos.
- [x] **Permite incorporar información previa (a priori) en la estimación de parámetros.**
- [ ] Reduce el tiempo de entrenamiento del modelo.
- [ ] No requiere datos previos para realizar predicciones.

**Explicación:** La belleza del enfoque de `[[Estadística Bayesiana]]` radica en el Teorema de Bayes, que permite actualizar dinámicamente nuestra creencia sobre una hipótesis combinando nuestra creencia inicial u opinión experta (`[[Probabilidad A Priori]]`) con la nueva evidencia recolectada.

---

## Pregunta 69
Un enfoque bayesiano para el análisis de datos es especialmente útil cuando:  

- [ ] Se quiere calcular la media aritmética de un conjunto de datos.
- [ ] No se dispone de datos históricos.
- [ ] Se tienen grandes cantidades de datos etiquetados.
- [x] **Se cuenta con información previa o conocimiento experto sobre el problema.**

**Explicación:** Si un cardiólogo sabe por experiencia que el 80% de un tipo de arritmia proviene del factor X, los `[[Modelos Bayesianos]]` permiten inyectar matemáticamente ese "conocimiento experto" en la `[[Probabilidad A Priori]]`, mejorando la inferencia aun con datos escasos.

---

## Pregunta 70
En un modelo bayesiano, ¿qué representa la distribución posterior?  

- [ ] La probabilidad de los datos dada una hipótesis.
- [x] **La probabilidad de una hipótesis dados los datos observados.**
- [ ] La probabilidad a priori de una hipótesis.
- [ ] La probabilidad marginal de los datos.

**Explicación:** La `[[Probabilidad Posterior]]` es la meta del Teorema de Bayes. Matemáticamente es $P(\text{Hipótesis} \mid \text{Datos})$. Responde a: "Después de observar esta nueva evidencia empírica, ¿qué tan cierta es ahora mi hipótesis?".

---

## Pregunta 71
Una determinada enfermedad afecta al 1% de la población. Una prueba para detectar la enfermedad tiene una sensibilidad del 95% (tasa de verdaderos positivos). Si una persona da positivo, ¿cuál es la probabilidad de que realmente tenga la enfermedad?  

- [ ] 0.171
- [x] **0.161**
- [ ] 0.191
- [ ] 0.181

**Explicación:** Asumiendo simetría estadística (Sensibilidad = Especificidad = 95%, por lo tanto, la tasa de falsos positivos es 5%), usamos `[[Teorema de Bayes]]`:
$P(\text{Enfermo} \mid \text{Positivo}) = \frac{(0.95 \times 0.01)}{(0.95 \times 0.01) + (0.05 \times 0.99)}$
$= \frac{0.0095}{0.0095 + 0.0495} = \frac{0.0095}{0.0590} = 0.16101 \dots \approx 0.161$.

---

## Pregunta 72
¿Cuál es la función de activación más utilizada en la capa de salida de una red neuronal para un problema de clasificación multiclase?  

- [ ] Tangente hiperbólica.
- [ ] ReLU.
- [x] **"Softmax".**
- [ ] Sigmoide.

**Explicación:** Para clasificación multiclase, la capa final debe generar probabilidades que sumen exactamente 1.0 (o 100%). La función `[[Softmax]]` toma un vector de números reales y los normaliza exponencialmente en una distribución de probabilidad sobre $K$ clases posibles.

---

## Pregunta 73
En un modelo bayesiano, ¿cómo se denomina la distribución de probabilidad que refleja el conocimiento previo antes de observar los datos?  

- [ ] Distribución marginal.
- [ ] Distribución condicional.
- [ ] Distribución posterior.
- [x] **Distribución a priori.**

**Explicación:** Como se deriva de la `[[Estadística Bayesiana]]`, la `[[Probabilidad A Priori (Prior)]]` representa matemáticamente nuestras creencias o certidumbre inicial sobre un parámetro antes de que cualquier nuevo experimento o recolección de datos tome lugar.

---
