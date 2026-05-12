# Sesion 1 - Probabilidad y Estadística
- Cadenas de Markov
- Análisis de regresión lineal simple, múltiple, logística
- Correlación
- ANOVA
- Distribuciones multivariadas
## Pregunta 1
Dada la siguiente matriz de transición de una cadena de Markov con tres estados:

$\begin{bmatrix}0.2 & 0.5 & 0.3 \\0.1 & 0.6 & 0.3 \\0.4 & 0.3 & 0.3 \\\end{bmatrix}$

si el sistema inicia en el estado 2 ($S_2$), ¿cuál es la probabilidad de que en el siguiente paso se encuentre en el estado 3 ($S_3$)?

- [ ] 0.5
- [ ] 0.1
- [ ] 0.6
- [x] **0.3**

**Explicación:** En una [[Cadena de Markov]], las filas representan el estado actual y las columnas el estado siguiente. La fila 2 (Estado $S_2$) indica las probabilidades de transición hacia $S_1$, $S_2$ y $S_3$ respectivamente. El valor en la fila 2, columna 3 es `0.3`, que representa la [[Probabilidad de transición]] de ir de $S_2$ a $S_3$.

---

## Pregunta 2
Se tiene una cadena de Markov con estados ($S_1$,$S_2$,$S_3$). Si se sabe que el sistema está en el estado $S_2$ en el tiempo $t$, ¿cómo se calcula la probabilidad de que en el tiempo $t+1$ el sistema esté en el estado $S_3$?

- [ ] Se usa la ley de los grandes números para estimar la probabilidad empírica.
- [ ] Se debe conocer toda la historia previa de la cadena para calcular la probabilidad de transición.
- [ ] Se calcula sumando las probabilidades de transición desde todos los estados anteriores al estado $S_3$.
- [x] **Se obtiene directamente de la matriz de probabilidades de transición, considerando solo el estado actual $S_2$.**

**Explicación:** La propiedad fundamental de las [[Cadenas de Markov]] es la "falta de memoria" (propiedad de Markov), lo que significa que el estado futuro solo depende del estado actual y no de la historia pasada. Por lo tanto, basta con ver la celda correspondiente al estado actual y futuro en la matriz.

---

## Pregunta 3
En la ecuación de regresión $Y=B_0+B_1X$, $B_1$ representa:

- [ ] La variable dependiente.
- [ ] La ordenada al origen.
- [ ] La variable independiente.
- [x] **La pendiente del modelo.**

**Explicación:** En un modelo de [[Regresión lineal simple]], $B_0$ es el intercepto (ordenada al origen) y $B_1$ representa la pendiente. La pendiente indica cuánto cambia en promedio la [[Variable dependiente]] (Y) por cada unidad de incremento en la [[Variable independiente]] (X).

---

## Pregunta 4
Un investigador quiere analizar la relación entre las horas de estudio y el puntaje obtenido en un examen. Decide ajustar un modelo de regresión lineal simple de la forma: $Y=B_0+B_1X+\epsilon$


Si $X$ representa el número de horas de estudio e $Y$ el puntaje en el examen, ¿cuál de las siguientes afirmaciones es correcta?

- [ ] $X$ es la variable dependiente porque es la que se quiere predecir.
- [ ] La variable dependiente es la que tiene un coeficiente más grande en el modelo.
- [ ] Ninguna es la variable dependiente, ya que en la regresión lineal simple no hay distinción entre dependiente e independiente.
- [x] **$Y$ es la variable dependiente porque es el resultado que se intenta explicar a partir de $X$.**

**Explicación:** En cualquier análisis de regresión, a la variable que buscamos estimar, predecir o explicar se le conoce como la [[Variable dependiente]] (comúnmente denotada como Y), que aquí es el puntaje. Las variables que usamos como predictores son las [[Variables independientes]] (X).

---

## Pregunta 5
Observa con atención el siguiente diagrama de dispersión, que representa un modelo de regresión lineal simple:

![[Pasted image 20260510181756.png]]

Con base en el diagrama y la ecuación del modelo, ¿cuál de las siguientes opciones representa correctamente la variable dependiente en el modelo de regresión lineal?

- [ ] La variable dependiente del modelo de regresión es $B0+B1X+e$
- [ ] La variable dependiente del modelo es B0+B1X
- [ ] La variable dependiente del modelo de regresión lineal es X
- [x] **La variable dependiente del modelo es Y**

**Explicación:** La [[Variable dependiente]] siempre es la variable respuesta que se ubica en el eje Y del gráfico de dispersión y es representada matemáticamente por la letra $Y$ en la ecuación de la regresión.

---

## Pregunta 6
En un modelo de regresión lineal múltiple, la suposición de homocedasticidad implica que:

- [ ] Los residuos tienen una distribución normal.
- [ ] Las variables independientes no están correlacionadas.
- [ ] Ninguna de las anteriores.
- [x] **Los residuos tienen una varianza constante.**

**Explicación:** La [[Homocedasticidad]] es un supuesto fundamental en los modelos de regresión lineal, el cual dicta que la dispersión (varianza) de los errores/residuos se mantiene constante a lo largo de todos los valores de las variables explicativas.

---

## Pregunta 7
¿Cuál es la principal razón por la que se verifica la normalidad de los residuos en un modelo de regresión lineal múltiple?

- [ ] Porque la normalidad de los residuos es necesaria para calcular el coeficiente de determinación $R^2$
- [ ] Porque la normalidad de los residuos garantiza que los coeficientes de regresión sean óptimos.
- [ ] Porque un modelo con residuos no normales no puede utilizarse para predecir valores futuros.
- [x] **Porque la inferencia estadística (pruebas de hipótesis e intervalos de confianza) se basa en la suposición de normalidad de los errores.**

**Explicación:** Si bien las predicciones y los coeficientes pueden calcularse sin normalidad, las pruebas estadísticas como los [[Valores p]] y los intervalos de confianza requieren que los residuos sigan una [[Distribución normal]] para que sus resultados sean válidos.

---

## Pregunta 8
¿Cuál de las siguientes opciones NO es una suposición del modelo de regresión lineal múltiple?

- [ ] Linealidad.
- [ ] Homocedasticidad.
- [ ] No multicolinealidad.
- [x] **Todas las variables independientes deben ser categóricas.**

**Explicación:** En la [[Regresión lineal múltiple]], las variables independientes pueden ser de cualquier tipo (numéricas continuas, discretas o categóricas convertidas en variables dummy). No es obligatorio que sean exclusivamente categóricas.

---

## Pregunta 9
Un economista construye un modelo de regresión lineal múltiple para predecir el ingreso mensual de una persona en función de:
X1: Años de educación.
X2: Experiencia laboral en años.
X3: Género (1 si es hombre, 0 si es mujer).

Tras estimar el modelo, obtiene: $Y = 2000 + 500(X1) + 300(X2) - 800(X3)$

¿Cuál es la interpretación correcta del coeficiente asociado a X3 en este modelo?

- [ ] No se puede interpretar el coeficiente de X3 porque es una variable categórica.
- [ ] El coeficiente de X3 indica que los ingresos dependen únicamente del género, sin importar la educación o experiencia laboral.
- [ ] Los hombres ganan en promedio $800 más que las mujeres, manteniendo constantes los otros factores.
- [x] **Las mujeres ganan en promedio $800 más que los hombres, manteniendo constantes los otros factores.**

**Explicación:** Como la variable X3 vale 1 para hombres, el término $-800(X3)$ resta 800 al estimado del hombre. Esto significa que los hombres ganan $800 menos que las mujeres, o visto de otra forma, que las mujeres (que son la categoría de referencia con X3=0) ganan $800 más que los hombres, manteniendo el resto de las [[Variables independientes]] constantes.

---

## Pregunta 10
¿Cuál de los siguientes métodos se usa para detectar la presencia de multicolinealidad en un modelo de regresión lineal múltiple?

- [ ] La prueba de Durbin-Watson
- [ ] La prueba de Levene
- [ ] La prueba de Shapiro-Wilk
- [x] **El estadístico de inflación de la varianza (VIF)**

**Explicación:** El [[Factor de Inflación de la Varianza]] (VIF) es una métrica empleada para identificar la [[Multicolinealidad]]. Nos dice qué tanto se infla la varianza de un coeficiente estimado debido a la alta correlación entre las variables independientes.

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

**Explicación:** Para validar el supuesto de [[Distribución normal]] en los residuos se utilizan herramientas gráficas, como el [[Histograma]] y el [[Gráfico Q-Q]], acompañadas de pruebas formales estadísticas como la [[Prueba de Shapiro-Wilk]].

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

**Explicación:** En una tabla [[ANOVA]], el estadístico de prueba es el Valor F, y la decisión sobre si existen diferencias significativas reales se toma observando el [[Valor p]] asociado. Un p-valor pequeño (menor que el nivel de significancia) indica que los grupos sí tienen medias diferentes.

---

## Pregunta 28
Un investigador educativo quiere analizar si existen diferencias significativas en las calificaciones promedio de estudiantes de tres colegios diferentes (A, B y C). Para ello, selecciona una muestra de estudiantes de cada colegio y aplica un ANOVA de una vía.

¿Cuáles son la hipótesis nula y la hipótesis alternativa en este estudio?

- [ ] H_0: La varianza de las calificaciones es la misma... H_1: La varianza es diferente...
- [x] **H_0: Todos los colegios tienen la misma media de calificaciones. H_1: Al menos un colegio tiene una media de calificaciones diferente a los demás.**
- [ ] H_0: No hay relación entre el colegio... H_1: La calificación depende del colegio...
- [ ] H_0: La media de calificaciones del Colegio A es mayor... H_1: La media del Colegio B es menor...

**Explicación:** El objetivo del [[ANOVA de una vía]] es comparar medias. Por definición, la [[Hipótesis nula]] postula que no hay diferencias (todas las medias poblacionales son iguales, $\mu_A = \mu_B = \mu_C$), mientras que la [[Hipótesis alternativa]] establece que al menos una media grupal difiere de las demás.

---

## Pregunta 29
Un investigador quiere analizar si existen diferencias significativas en el rendimiento académico de tres grupos de estudiantes que recibieron distintos métodos de enseñanza: presencial, en línea y mixto. Para ello, recopila las calificaciones finales de los estudiantes y aplica un ANOVA de una vía.

¿Cuál es el objetivo principal de la tabla ANOVA en este contexto?

- [ ] Comprobar si los datos cumplen con los supuestos de normalidad y homocedasticidad.
- [ ] Determinar si la varianza total de las calificaciones es mayor en algunos grupos que en otros.
- [ ] Estimar el efecto del método de enseñanza en la distribución normal de las calificaciones.
- [x] **Evaluar si la media de al menos un grupo es significativamente diferente de las demás.**

**Explicación:** El [[ANOVA]] (Análisis de Varianza) a pesar de su nombre, se utiliza primordialmente para comparar si las medias numéricas de tres o más grupos difieren estadísticamente entre sí.

---