# **Lista de Ejercicios - Sesión 3** - Ciencia de Datos ​
- Analítica de datos
- Adquisión y preparación de datos​
- Métodos Gráficos​
- Modelos ARIMA, SARIMA para series de tiempo
## Pregunta 1
Determinar cuales de los siguientes subconjuntos de $\mathbb{R}$ son cerrados bajo la topología estándar. (Elegir todas las respuestas correctas.)  

- [ ] $(0,\infty)$
- [x] **$[0,\infty)$**
- [x] **$[0,1]$**
- [ ] $(0,1]$

**Explicación:** En topología, un conjunto es [[Conjunto cerrado]] si contiene todos sus puntos límite. Los intervalos que incluyen sus extremos (representados por corchetes `[` o `]`) son cerrados. Por ende, tanto $[0,1]$ como $[0,\infty)$ son cerrados en $\mathbb{R}$.

---

## Pregunta 2
Consideremos el toro $T=S^{1}\times S^{1}$, donde $S^{1}=\{(x,y)\in \mathbb{R}^{2} \mid x^{2}+y^{2}=1\}$ es el círculo unitario. ¿Cuáles son los números de Betti del toro $T$?  

- [ ] (2,1,2)
- [x] **(1,2,1)**
- [ ] (1,1,1)
- [ ] (1,0,1)

**Explicación:** En [[Topología Algebraica]], los [[Números de Betti]] $(b_0, b_1, b_2)$ representan la cantidad de características topológicas en cada dimensión. Para un toro, $b_0=1$ (un componente conectado), $b_1=2$ (dos lazos o ciclos 1-dimensionales independientes), y $b_2=1$ (una cavidad 2-dimensional hueca en su interior).

---

## Pregunta 3
¿Por qué es útil el análisis topológico de datos en el análisis de conjuntos de datos de alta dimensión?  

- [ ] Etiqueta los datos de manera automática
- [x] **Nos ayuda a encontrar estructuras estables en nuestro conjunto de datos que son independientes de la escala**
- [ ] Puede reducir el número de dimensiones sin perder información
- [ ] Nos ayuda a eliminar el ruido en los datos

**Explicación:** El [[Análisis Topológico de Datos (TDA)]] utiliza herramientas como la [[Homología Persistente]] para identificar la "forma" de los datos (agujeros, vacíos, clusters) que persiste a través de diferentes escalas espaciales, extrayendo características topológicas robustas.

---

## Pregunta 4
¿Cuál de las siguientes afirmaciones sobre la **varianza** es **correcta**?  

- [ ] La varianza siempre tiene las mismas unidades que los datos originales.
- [x] **Si la varianza es cero, todos los valores en el conjunto de datos son iguales.**
- [ ] La varianza mide la tendencia central de los datos.
- [ ] La varianza puede tomar valores negativos si los datos están sesgados.

**Explicación:** La [[Varianza]] mide la dispersión cuadrática de los datos respecto a su media. Si es exactamente 0, significa que no hay dispersión y todos los puntos de datos son idénticos.

---

## Pregunta 5
¿Cuál de las siguientes no es una medida de dispersión?  

- [ ] Desviación estándar.
- [ ] Rango intercuartílico.
- [ ] Varianza.
- [x] **Moda.**

**Explicación:** La [[Moda]] es una [[Medida de tendencia central]] (indica el valor más frecuente), mientras que la varianza, desviación estándar y rango intercuartílico son medidas de dispersión estadística.

---

## Pregunta 6
¿Cuál de los siguientes conjuntos de medidas de dispersión se ve más afectado por valores atípicos en un conjunto de datos?  

- [ ] El rango intercuartílico y la mediana.
- [ ] La moda y el rango intercuartílico.
- [x] **La varianza y la desviación estándar.**
- [ ] La mediana y la desviación media absoluta.

**Explicación:** Al ser derivadas del cuadrado de las diferencias entre cada dato y la media, la [[Varianza]] y la [[Desviación estándar]] amplifican exponencialmente el impacto numérico de los [[Valores atípicos (Outliers)]].

---

## Pregunta 7
Si se añade un **valor extremo muy alto** a un conjunto de datos, ¿qué medida de tendencia central se verá más afectada?  

- [x] **La media**
- [ ] La moda
- [ ] La mediana
- [ ] Ninguna, ya que todas son resistentes a valores extremos

**Explicación:** La `[[Media aritmética]]` considera la magnitud cuantitativa de todos los datos en su cálculo. Un valor excesivamente grande empujará el promedio aritmético significativamente hacia ese extremo.

---

## Pregunta 8
¿Cuál de las siguientes **afirmaciones sobre el rango intercuartílico (IQR)** es **verdadera**?  

- [x] **El IQR mide la diferencia entre el primer y tercer cuartil, abarcando el 50% central de los datos.**
- [ ] Un IQR de cero significa que la distribución es simétrica.
- [ ] Si el IQR es pequeño, significa que la media también es pequeña.
- [ ] El IQR se ve muy afectado por valores atípicos extremos.

**Explicación:** El `[[Rango Intercuartílico (IQR)]]` se calcula como $Q3 - Q1$, eliminando el 25% superior y el 25% inferior, por lo que describe exactamente la dispersión del 50% central de los datos y es robusto ante atípicos.

---

## Pregunta 9
¿Qué indica el valor p en una prueba de hipótesis?  

- [ ] El valor más probable del parámetro poblacional.
- [ ] La probabilidad de que la hipótesis nula sea verdadera.
- [x] **La probabilidad de observar un estadístico al menos tan extremo como el observado, asumiendo que la hipótesis nula es verdadera.**
- [ ] La probabilidad de que la hipótesis alternativa sea verdadera.

**Explicación:** En la `[[Inferencia estadística]]`, el `[[Valor p]]` o p-valor es una medida probabilística de la evidencia contra la hipótesis nula ($H_0$). Si es bajo, sugiere que los datos observados son muy inusuales si $H_0$ fuera correcta.

---

## Pregunta 10
¿Qué tipo de prueba estadística es más adecuada para analizar la relación entre dos variables categóricas?  

- [ ] Prueba t de Student.
- [ ] Análisis de varianza (ANOVA).
- [x] **Prueba de chi-cuadrado.**
- [ ] Regresión lineal.

**Explicación:** La `[[Prueba Chi-Cuadrado]]` de independencia es el test por excelencia para determinar si existe una asociación estadísticamente significativa entre dos variables categóricas o cualitativas.

---

## Pregunta 11
¿Cuál de las siguientes afirmaciones es verdadera acerca de los intervalos de confianza?  

- [x] **Un intervalo de confianza del 95% significa que el parámetro poblacional está dentro del intervalo en el 95% de las muestras.**
- [ ] Un intervalo de confianza siempre incluye la media de la población.
- [ ] Un intervalo de confianza más amplio indica mayor precisión en la estimación.
- [ ] Un intervalo de confianza se usa para estimar parámetros de la muestra, no de la población.

**Explicación:** La interpretación frecuentista de un `[[Intervalo de confianza]]` del 95% señala que si se extrajeran múltiples muestras aleatorias bajo las mismas condiciones y se calcularan intervalos para todas, alrededor del 95% de esos intervalos contendrían el verdadero parámetro de la población.

---

## Pregunta 12
¿Qué significa un **p-valor** de 0.03 en una prueba de hipótesis?  

- [ ] Que la hipótesis alternativa debe ser aceptada sin ninguna duda.
- [x] **Que si la hipótesis nula fuera cierta, la probabilidad de obtener un resultado tan extremo como el observado sería del 3%.**
- [ ] Que la hipótesis nula es verdadera con un 97% de confianza.
- [ ] Que hay un 3% de probabilidad de que la hipótesis alternativa sea verdadera.

**Explicación:** Un `[[Valor p]]` del 0.03 (3%) es la probabilidad condicional de obtener la misma estadística observada asumiendo ciegamente que la hipótesis nula es cierta. Generalmente, un valor menor a 0.05 es suficiente para rechazar $H_0$.

---

## Pregunta 13
¿Qué tipo de gráfico es más adecuado para visualizar la distribución de una variable cuantitativa?  

- [ ] Gráfico de barras
- [x] **Histograma**
- [ ] Diagrama de dispersión
- [ ] Diagramas de caja

**Explicación:** El `[[Histograma]]` agrupa los datos cuantitativos continuos en rangos (bins) continuos y muestra su frecuencia, revelando instantáneamente la forma, la simetría y la distribución (ej. Normal, sesgada) de los datos.

---

## Pregunta 14
¿Cuál es el objetivo principal de la inferencia estadística?  

- [ ] Normalizar los datos
- [x] **Extraer conclusiones sobre una población a partir de una muestra**
- [ ] Describir un conjunto de datos
- [ ] Eliminar el ruido en los datos

**Explicación:** A diferencia de la estadística descriptiva, la `[[Inferencia estadística]]` utiliza las matemáticas y el muestreo aleatorio para estimar y generalizar propiedades de una `[[Población]]` entera utilizando solo una fracción de los datos (`[[Muestra]]`).

---

## Pregunta 15
Dado el siguiente DataFrame:
`df = pd.DataFrame({'Nombre': ['Ana', 'Luis', 'Carlos', 'Sofia'], 'Edad': [25, 30, 35, 28]})`

¿Qué expresión devuelve solo las filas donde la edad es mayor a 28?  

- [ ] `df.loc[df['Edad'] < 28]`
- [ ] `df.loc[df['Edad'] >= 28]`
- [x] **`df.query("Edad > 28")`**
- [ ] `df.query(Edad > 28)`

**Explicación:** En `[[Pandas]]`, `.query()` acepta una cadena o string con una condición booleana para filtrar el `[[DataFrame]]` fácilmente.

---

## Pregunta 16
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

## Pregunta 17
En ciencia de datos ¿Qué se entiende por transformación de datos?  

- [x] **Aplicar técnicas como escalado, normalización o logaritmos**
- [ ] Cambiar la estructura del conjunto de datos
- [ ] Eliminar variables no significativas
- [ ] Convertir datos cualitativos en cuantitativos

**Explicación:** La `[[Transformación de datos]]` en Machine Learning típicamente se refiere a procesos matemáticos y estadísticos (como `[[Normalización]]` o `[[Estandarización]]`) que ajustan la escala y distribución de las variables para optimizar los algoritmos predictivos.

---

## Pregunta 18
¿Cuál de los siguientes formatos de archivo es más eficiente para almacenar grandes volúmenes de datos estructurados?  

- [ ] CSV
- [ ] JSON
- [ ] TXT
- [x] **Parquet**

**Explicación:** `[[Apache Parquet]]` es un formato de archivo orientado a columnas y altamente comprimido que está diseñado para el ecosistema Hadoop y Big Data, siendo infinitamente más rápido y ligero en memoria que formatos de texto plano como CSV.

---

## Pregunta 19
¿Qué información clave proporciona un **gráfico de dispersión** en un análisis estadístico?  

- [ ] La distribución de una variable categórica.
- [ ] La correlación exacta entre dos variables.
- [ ] La varianza de una única variable.
- [x] **La relación entre dos variables cuantitativas.**

**Explicación:** El `[[Diagrama de dispersión]]` o Scatter plot mapea dos variables continuas numéricas en los ejes X e Y. Esto permite identificar visualmente la relación, tendencia (lineal o no lineal), agrupaciones y presencia de outliers entre ambas.

---

## Pregunta 20
En un **gráfico de cajas y bigotes (boxplot)**, ¿qué indica la longitud de los bigotes?  

- [x] **La dispersión de los datos dentro de 1.5 veces el rango intercuartílico (IQR).**
- [ ] La cantidad de datos en el conjunto.
- [ ] El valor exacto de la media.
- [ ] La correlación entre dos variables.

**Explicación:** Por convención de John Tukey, los bigotes de un `[[Boxplot]]` se extienden desde el extremo de la caja (los cuartiles 1 y 3) hasta abarcar el valor más extremo disponible que se encuentre a una distancia matemática no mayor a $1.5 \times IQR$. Los datos fuera de este rango se marcan como valores atípicos.

---

## Pregunta 21
¿Cuál es la ventaja principal de usar gráficos interactivos en análisis de datos?  

- [ ] General análisis automáticos
- [ ] Reducen el tamaño del conjunto de datos
- [x] **Permiten filtrar y explorar los datos en profundidad**
- [ ] Aumentan la precisión de los modelos predictivos

**Explicación:** En la `[[Visualización de datos]]`, los gráficos dinámicos (usando herramientas como Plotly o Dash) permiten a los usuarios hacer zoom, seleccionar subconjuntos y pasar el cursor para leer valores exactos (`tooltips`), mejorando drásticamente el análisis exploratorio (EDA).

---

## Pregunta 22
¿Cuál de los siguientes gráficos es más útil para visualizar la relación entre dos variables numéricas?  

- [ ] Gráfico de barras
- [ ] Gráfico de pastel
- [x] **Diagrama de dispersión**
- [ ] Histograma

**Explicación:** Al igual que en la pregunta 19, el `[[Diagrama de dispersión]]` permite situar valores numéricos a lo largo de un eje cartesiano, siendo la representación óptima y nativa para correlacionar dos valores continuos.

---

## Pregunta 23
¿Cuál de los siguientes pasos es fundamental antes de aplicar un modelo ARIMA a una serie de tiempo?  

- [x] **Comprobar la estacionariedad**
- [ ] Usar one-hot enconding
- [ ] Realizar una regresión lineal
- [ ] Convertir la serie en datos categóricos

**Explicación:** Un supuesto riguroso y esencial del modelo matemático de `[[Series de Tiempo]]` `[[ARIMA]]` es que la varianza y la media sean constantes en el tiempo. Por ello, el análisis siempre requiere comprobar (o forzar a través de integración "I") la `[[Estacionariedad]]` de la serie primero mediante tests como Dickey-Fuller.

---

## Pregunta 24
¿Qué método se puede usar para determinar los valores óptimos de "p" y "q" en un modelo ARIMA?  

- [ ] Test de normalidad
- [ ] Regresión logística
- [x] **Autocorrelación y autocorrelación parcial**
- [ ] Método del codo

**Explicación:** En el ajuste del modelo estadístico `[[ARIMA]]` (p,d,q), se examinan las funciones de `[[Autocorrelación (ACF)]]` y la `[[Autocorrelación parcial (PACF)]]`. La ACF ayuda a inferir "q" (componente de Media Móvil o MA), y la PACF determina "p" (componente Autorregresivo o AR).

---

## Pregunta 25
Lee con atención los siguientes enunciados y selecciona la opción que explique correctamente cómo se pueden emplear los componentes principales en el análisis de datos.  

- [x] **Las componentes principales son los eigenvectores de la matriz de covarianza y representan las direcciones con mayor variabilidad en los datos. Se pueden usar para reducir el número de variables en un modelo de clasificación sin perder demasiada información.**
- [ ] Las componentes principales son los eigenvectores de la matriz de covarianza y representan las direcciones con menor variabilidad...
- [ ] Las componentes principales son combinaciones aleatorias de las variables originales...
- [ ] Las componentes principales indican las direcciones con menor variabilidad... provienen de la matriz Hessiana...

**Explicación:** El `[[Análisis de Componentes Principales (PCA)]]` es una técnica algebraica de `[[Reducción de dimensionalidad]]`. Mediante eigenvectores, extrae nuevas variables (componentes) perpendiculares entre sí, proyectando los datos donde se captura su máxima varianza, preservando su estructura matemática reduciendo la carga de cómputo.

---

## Pregunta 26
Consideremos la esfera unitaria $S^{2}=\{(x,y,z)\in \mathbb{R}^{3}\mid x^{2}+y^{2}+z^{2}=1\}$. ¿Cuáles son sus números de Betti?  

- [ ] (1,2,1)
- [ ] (1,1,1)
- [ ] (2,1,2)
- [x] **(1,0,1)**

**Explicación:** En `[[Topología Algebraica]]`, los `[[Números de Betti]]` de una esfera $S^2$ son $b_0=1$ (porque tiene una sola componente conectada), $b_1=0$ (no tiene lazos unidimensionales o túneles, todo lazo se puede contraer a un punto), y $b_2=1$ (tiene una sola cavidad tridimensional o volumen encerrado).

---

## Pregunta 27
¿Cuál es el rol de una filtración en la homología persistente?  

- [x] **Identificar la evolución de las características topológicas del conjunto de datos a distintas escalas**
- [ ] Calcular la transformada de Fourier del conjunto de datos
- [ ] Generar muestras aleatorias a partir del conjunto de datos
- [ ] Eliminar los puntos con ruido

**Explicación:** En el `[[Análisis Topológico de Datos (TDA)]]`, una filtración crea una secuencia anidada de espacios topológicos. Esto permite observar en qué momento nacen y mueren las características geométricas (agujeros, componentes), revelando las estructuras que "persisten" en distintas escalas.

---

## Pregunta 28
¿Qué medida de tendencia central es más sensible a los valores atípicos en un conjunto de datos?  

- [ ] Rango.
- [x] **Media.**
- [ ] Moda.
- [ ] Mediana.

**Explicación:** La `[[Media aritmética]]` es extremadamente sensible a `[[Valores atípicos (Outliers)]]`, ya que incluye todos y cada uno de los valores en su sumatoria. Un solo valor extremo puede desplazarla artificialmente hacia la derecha o izquierda.

---

## Pregunta 29
Si la media de un conjunto de datos es 50 y la mediana es 40, ¿cómo está sesgada la distribución?  

- [ ] No hay sesgo.
- [x] **Sesgo a la derecha.**
- [ ] Sesgo a la izquierda.
- [ ] No se puede determinar.

**Explicación:** Cuando la `[[Media aritmética]]` es mayor que la `[[Mediana]]`, significa que existen valores atípicamente altos que están "jalando" el promedio aritmético hacia valores positivos, lo que genera un `[[Sesgo a la derecha (Asimetría positiva)]]`.

---

## Pregunta 30
Un investigador quiere determinar si el tiempo promedio que tardan los clientes en una tienda ha cambiado con respecto al año pasado. ¿Cuál de las siguientes pruebas de hipótesis sería la más adecuada para este caso?  

- [ ] Prueba de chi-cuadrado de independencia.
- [x] **Prueba t para una muestra.**
- [ ] Prueba ANOVA.
- [ ] Prueba t para muestras independientes.

**Explicación:** Al comparar la media de una muestra actual contra un estándar histórico conocido ("el promedio del año pasado"), la metodología estadísticamente correcta es una `[[Prueba T de Student]]` para una sola muestra (One-Sample T-Test).

---

## Pregunta 31
En una prueba t de Student para dos muestras independientes, ¿cuál es el propósito de esta prueba?  

- [x] **Comparar las medias de dos muestras independientes para determinar si son significativamente diferentes.**
- [ ] Comparar la media de una muestra con una media conocida de la población.
- [ ] Comparar las medias de dos muestras dependientes.
- [ ] Comparar la mediana de dos muestras para determinar la igualdad de distribuciones.

**Explicación:** La `[[Prueba T de Student para muestras independientes]]` se diseña específicamente para evaluar si las `[[Media aritmética|Medias]]` poblacionales de dos grupos mutuamente excluyentes y no relacionados difieren de forma estadísticamente significativa.

---

## Pregunta 32
¿Cuál de los siguientes es un error de tipo I en una prueba de hipótesis?  

- [ ] No rechazar la hipótesis nula cuando es falsa.
- [x] **Rechazar la hipótesis nula cuando es verdadera.**
- [ ] Aceptar la hipótesis nula cuando es falsa.
- [ ] No rechazar la hipótesis alternativa cuando es verdadera.

**Explicación:** En la `[[Inferencia estadística]]`, el `[[Error de Tipo I]]` (Falso Positivo) ocurre al descartar la $H_0$ a pesar de que ésta era la correcta en la realidad. Equivale a detectar un efecto estadístico donde realmente no lo hay.

---

## Pregunta 33
Si realizas una prueba de hipótesis con un nivel de significancia $\alpha=0.05$, ¿qué significa esto?  

- [ ] Existe un chance del 95% de aceptar la hipótesis nula.
- [ ] Existe un chance del 5% de que la hipótesis alternativa sea falsa.
- [ ] Existe un chance del 95% de que la hipótesis nula sea verdadera.
- [x] **Existe un chance del 5% de rechazar incorrectamente la hipótesis nula cuando es verdadera.**

**Explicación:** El `[[Nivel de significancia (Alfa)]]` define exactamente la probabilidad máxima permitida de cometer un `[[Error de Tipo I]]`. Un $\alpha=0.05$ establece que toleraremos un 5% de probabilidad de rechazar una hipótesis nula cierta (falso positivo).

---

## Pregunta 34
¿Qué prueba estadística se usa para comparar las medias de dos grupos independientes?  

- [ ] ANOVA
- [x] **Prueba t de Student**
- [ ] Chi-cuadrado
- [ ] Regresión lineal

**Explicación:** Como se vio previamente, la `[[Prueba T de Student]]` es el método paramétrico estándar para evaluar la diferencia de medias entre dos, y solo dos, grupos no correlacionados.

---

## Pregunta 35
¿Cuál de las siguientes medidas NO es una medida de dispersión?  

- [ ] Varianza
- [x] **Media**
- [ ] Rango
- [ ] Desviación estándar

**Explicación:** La `[[Media aritmética]]` es una `[[Medida de tendencia central]]`, diseñada para hallar el punto de equilibrio o centro de la distribución. La varianza, el rango y la desviación estándar sí miden la separación o dispersión numérica de los datos.

---

## Pregunta 36
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

## Pregunta 37
¿Qué técnica se usa comúnmente para manejar valores faltantes en un conjunto de datos?  

- [ ] Eliminación de registros
- [x] **Todas las anteriores**
- [ ] Imputación con la media
- [ ] Uso de modelos predictivos

**Explicación:** En el proceso de `[[Limpieza de datos]]`, el manejo de valores nulos o `[[Valores faltantes (Missing values)]]` puede abordarse matemáticamente rellenando (imputando) con estadísticas simples o complejas (medias, modelos), o directamente borrando las observaciones problemáticas.

---

## Pregunta 38
¿Qué problema se soluciona con la técnica de "one-hot encoding"?  

- [ ] Valores atípicos en los datos
- [ ] Reducción de dimensionalidad
- [x] **Codificación de variables categóricas en valores numéricos**
- [ ] Falta de datos en algunas filas

**Explicación:** El `[[One-Hot Encoding]]` soluciona el problema de que los algoritmos matemáticos no entienden categorías en texto. Crea múltiples columnas binarias, evitando además asumir un orden jerárquico artificial entre las categorías.

---

## Pregunta 39
¿Qué gráfica se utiliza para identificar valores atípicos y la distribución general de un conjunto de datos?  

- [x] **Diagrama de caja.**
- [ ] Gráfico de líneas.
- [ ] Diagrama de Pareto.
- [ ] Diagrama de barras.

**Explicación:** El `[[Diagrama de caja (Boxplot)]]` resume maravillosamente la distribución en cuartiles, la asimetría, y además representa visualmente los valores individuales atípicos como puntos externos a sus "bigotes".

---

## Pregunta 40
¿Cuál de los siguientes gráficos se utiliza comúnmente para evaluar la relación entre los valores observados y los valores predichos en la regresión lineal?  

- [x] **Diagrama de dispersión.**
- [ ] Gráfico de barras.
- [ ] Histograma.
- [ ] Diagrama de cajas.

**Explicación:** En un análisis de predicción (`[[Regresión lineal]]`), situamos los valores reales observados en el eje Y y los predichos en el eje X dentro de un `[[Diagrama de dispersión]]` para observar gráficamente qué tan cerca están de la línea identidad perfecta.

---

## Pregunta 41
¿Qué gráfico es ideal para detectar valores atípicos en un conjunto de datos?  

- [ ] Gráfico de pastel
- [ ] Gráfico de radar
- [ ] Gráfico de líneas
- [x] **Boxplot**

**Explicación:** Esta es otra forma de validar la utilidad del `[[Boxplot]]`. Al trazar un límite analítico (generalmente de $1.5 \times IQR$), identifica de manera automática e imparcial a los datos extremos u outliers.

---

## Pregunta 42
¿Cuál de los siguientes modelos es más adecuado para analizar series de tiempo con un componente estacional?  

- [ ] Regresión lineal
- [ ] K-means
- [x] **SARIMA**
- [ ] ARIMA

**Explicación:** Para problemas con estacionalidad cíclica clara (como subidas de ventas en diciembre), `[[ARIMA]]` clásico falla. Por eso se creó la variante **Seasonal-ARIMA** (`[[SARIMA]]`), que añade hiperparámetros estacionales ($P,D,Q,m$) para capturar dichos patrones periódicos repetitivos.

---

## Pregunta 43
¿Qué hace la función de autocorrelación parcial (PACF) en el análisis de series de tiempo?  

- [x] **Mide la dependencia de un punto con su pasado después de eliminar efectos intermedios**
- [ ] Identifica patrones de tendencia
- [ ] Indica si la serie es estacionaria
- [ ] Predice valores futuros

**Explicación:** A diferencia de la ACF normal, la `[[Autocorrelación parcial (PACF)]]` aísla la relación estadística directa (o de "puro efecto") entre un dato en el tiempo $t$ y un valor pasado $t-k$, retirando la influencia de todos los periodos que existieron en el medio de ellos.

---

## Pregunta 44
Una empresa de análisis deportivo ha recopilado datos sobre el rendimiento de jugadores de baloncesto en **diferentes habilidades**, como **precisión en tiros, velocidad, resistencia y altura del salto**. Después de aplicar **Análisis de Componentes Principales (PCA)** a los datos, encuentran que el **primer componente principal (PC1)** tiene **altas cargas en velocidad y resistencia**, mientras que la precisión en tiros y la altura del salto tienen cargas menores.

**¿Cuál es la interpretación más adecuada de estos resultados?**  

- [x] **La velocidad y la resistencia explican la mayor parte de la variabilidad en el rendimiento de los jugadores.**
- [ ] Los jugadores más veloces y resistentes también tienen mejor precisión en tiros y mayor altura de salto.
- [ ] La precisión en tiros y la altura del salto son los factores más importantes para diferenciar a los jugadores.
- [ ] El PCA indica que los jugadores con mejor velocidad y resistencia son los mejores en todas las habilidades analizadas.  

**Explicación:** En `[[Análisis de Componentes Principales (PCA)]]`, el Componente 1 o PC1 siempre es la dirección donde existe la **mayor varianza**. Si este componente está fuertemente dominado por "velocidad y resistencia", entonces esas variables son los principales descriptores o "diferenciadores" numéricos entre un jugador y otro.

---

## Pregunta 45
Determinar cuales de los siguientes subconjuntos de $\mathbb{R}^{2}$ son conexos bajo la topología estándar. (Elegir todas las respuestas correctas.)  

- [ ] $\{(x,y)\in \mathbb{R}^{2} \mid x^{2}=1\}$
- [x] **$\{(x,y)\in \mathbb{R}^{2} \mid x^{2}=y^{2}\}$**
- [x] **$\{(x,y)\in \mathbb{R}^{2} \mid x^{2}+y^{2}=1\}$**
- [ ] $\{(x,y)\in \mathbb{R}^{2} \mid x^{2}-y^{2}=1\}$

**Explicación:** Un `[[Espacio conexo]]` es aquel que no puede dividirse en dos piezas disjuntas separadas. $x^2=1$ son dos líneas paralelas separadas; $x^2-y^2=1$ es una hipérbola con dos ramas separadas. Sin embargo, $x^2=y^2$ es una cruz o "X" conectada en el origen, y $x^2+y^2=1$ es un círculo continuo. Por tanto, estos dos últimos son conexos.

---

## Pregunta 46
¿Cuál de los siguientes enunciados describe mejor la interpretación de los números de Betti?  

- [ ] La media, varianza y asimetría estadística de los conjuntos de datos
- [ ] Las diferentes medias de nuestros datos
- [x] **El número de componentes conexas, lazos y hoyos en el espacio**
- [ ] El número total de vértices en una representación gráfica de los datos

**Explicación:** Los `[[Números de Betti]]` son invariantes topológicos que cuantifican las características de un espacio: $b_0$ cuenta las componentes conexas, $b_1$ los agujeros o túneles circulares bidimensionales, y $b_2$ las cavidades o vacíos tridimensionales.

---

## Pregunta 47
Si el **coeficiente de asimetría** de una distribución es **negativo**, ¿qué significa esto?  

- [x] **Que la distribución tiene una cola más larga hacia la izquierda.**
- [ ] Que la moda es mayor que la media y la mediana.
- [ ] Que la distribución es simétrica.
- [ ] Que la mediana es mayor que la moda, pero menor que la media.

**Explicación:** Un coeficiente de `[[Asimetría (Skewness)]]` negativo o sesgo a la izquierda ocurre cuando hay algunos valores atípicamente pequeños que alargan la cola del lado izquierdo de la distribución, jalando la media hacia valores inferiores.

---

## Pregunta 48
Dado el siguiente DataFrame:
`df = pd.DataFrame({'Categoria': ['A', 'B', 'A', 'B', 'A'], 'Valor': [10, 20, 30, 40, 50]})`

¿Qué operación devolvería la **suma de "Valor" para cada "Categoria"**?  

- [ ] `df.groupby('Valor')['Categoria'].sum()`
- [ ] `df.groupby('Categoria')['Valor'].count()`
- [ ] `df.groupby('Categoria').sum()`
- [x] **`df.groupby('Categoria')['Valor'].sum()`**

**Explicación:** En `[[Pandas]]`, la agregación se realiza usando `.groupby()`. Al agrupar por la columna `'Categoria'`, luego seleccionamos específicamente la columna a sumar (`['Valor']`) y aplicamos la función de reducción `.sum()`.

---

## Pregunta 49
En un diagrama de dispersión, ¿qué indica la presencia de una nube de puntos con una clara tendencia ascendente?  

- [ ] Una distribución normal
- [x] **Una correlación positiva**
- [ ] Una correlación negativa
- [ ] No hay relación entre las variables

**Explicación:** Al analizar un `[[Diagrama de dispersión]]`, una tendencia ascendente (de abajo izquierda a arriba derecha) visualiza que a medida que aumenta la variable X, también lo hace la variable Y, lo que define numéricamente una `[[Correlación de Pearson|Correlación positiva]]`.

---
