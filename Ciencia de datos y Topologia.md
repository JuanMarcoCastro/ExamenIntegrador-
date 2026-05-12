# 📚 Banco de Preguntas: Tema Topologia SeriesTiempo

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
¿Cuál de los siguientes formatos de archivo es más eficiente para almacenar grandes volúmenes de datos estructurados?  

- [ ] CSV
- [ ] JSON
- [ ] TXT
- [x] **Parquet**

**Explicación:** [[Apache Parquet]] es un formato de archivo orientado a columnas y altamente comprimido que está diseñado para el ecosistema Hadoop y Big Data, siendo infinitamente más rápido y ligero en memoria que formatos de texto plano como CSV.

---

## Pregunta 5
¿Cuál de los siguientes pasos es fundamental antes de aplicar un modelo ARIMA a una serie de tiempo?  

- [x] **Comprobar la estacionariedad**
- [ ] Usar one-hot enconding
- [ ] Realizar una regresión lineal
- [ ] Convertir la serie en datos categóricos

**Explicación:** Un supuesto riguroso y esencial del modelo matemático de [[Series de Tiempo]] [[ARIMA]] es que la varianza y la media sean constantes en el tiempo. Por ello, el análisis siempre requiere comprobar (o forzar a través de integración "I") la [[Estacionariedad]] de la serie primero mediante tests como Dickey-Fuller.

---

## Pregunta 6
Lee con atención los siguientes enunciados y selecciona la opción que explique correctamente cómo se pueden emplear los componentes principales en el análisis de datos.  

- [x] **Las componentes principales son los eigenvectores de la matriz de covarianza y representan las direcciones con mayor variabilidad en los datos. Se pueden usar para reducir el número de variables en un modelo de clasificación sin perder demasiada información.**
- [ ] Las componentes principales son los eigenvectores de la matriz de covarianza y representan las direcciones con menor variabilidad...
- [ ] Las componentes principales son combinaciones aleatorias de las variables originales...
- [ ] Las componentes principales indican las direcciones con menor variabilidad... provienen de la matriz Hessiana...

**Explicación:** El [[Análisis de Componentes Principales (PCA)]] es una técnica algebraica de [[Reducción de dimensionalidad]]. Mediante eigenvectores, extrae nuevas variables (componentes) perpendiculares entre sí, proyectando los datos donde se captura su máxima varianza, preservando su estructura matemática reduciendo la carga de cómputo.

---

## Pregunta 7
Consideremos la esfera unitaria $S^{2}=\{(x,y,z)\in \mathbb{R}^{3}\mid x^{2}+y^{2}+z^{2}=1\}$. ¿Cuáles son sus números de Betti?  

- [ ] (1,2,1)
- [ ] (1,1,1)
- [ ] (2,1,2)
- [x] **(1,0,1)**

**Explicación:** En [[Topología Algebraica]], los [[Números de Betti]] de una esfera $S^2$ son $b_0=1$ (porque tiene una sola componente conectada), $b_1=0$ (no tiene lazos unidimensionales o túneles, todo lazo se puede contraer a un punto), y $b_2=1$ (tiene una sola cavidad tridimensional o volumen encerrado).

---

## Pregunta 8
¿Cuál es el rol de una filtración en la homología persistente?  

- [x] **Identificar la evolución de las características topológicas del conjunto de datos a distintas escalas**
- [ ] Calcular la transformada de Fourier del conjunto de datos
- [ ] Generar muestras aleatorias a partir del conjunto de datos
- [ ] Eliminar los puntos con ruido

**Explicación:** En el [[Análisis Topológico de Datos (TDA)]], una filtración crea una secuencia anidada de espacios topológicos. Esto permite observar en qué momento nacen y mueren las características geométricas (agujeros, componentes), revelando las estructuras que "persisten" en distintas escalas.

---

## Pregunta 9
¿Cuál de los siguientes modelos es más adecuado para analizar series de tiempo con un componente estacional?  

- [ ] Regresión lineal
- [ ] K-means
- [x] **SARIMA**
- [ ] ARIMA

**Explicación:** Para problemas con estacionalidad cíclica clara (como subidas de ventas en diciembre), [[ARIMA]] clásico falla. Por eso se creó la variante **Seasonal-ARIMA** ([[SARIMA]]), que añade hiperparámetros estacionales ($P,D,Q,m$) para capturar dichos patrones periódicos repetitivos.

---

## Pregunta 10
Una empresa de análisis deportivo ha recopilado datos sobre el rendimiento de jugadores de baloncesto en **diferentes habilidades**, como **precisión en tiros, velocidad, resistencia y altura del salto**. Después de aplicar **Análisis de Componentes Principales (PCA)** a los datos, encuentran que el **primer componente principal (PC1)** tiene **altas cargas en velocidad y resistencia**, mientras que la precisión en tiros y la altura del salto tienen cargas menores.

**¿Cuál es la interpretación más adecuada de estos resultados?**  

- [x] **La velocidad y la resistencia explican la mayor parte de la variabilidad en el rendimiento de los jugadores.**
- [ ] Los jugadores más veloces y resistentes también tienen mejor precisión en tiros y mayor altura de salto.
- [ ] La precisión en tiros y la altura del salto son los factores más importantes para diferenciar a los jugadores.
- [ ] El PCA indica que los jugadores con mejor velocidad y resistencia son los mejores en todas las habilidades analizadas.  

**Explicación:** En [[Análisis de Componentes Principales (PCA)]], el Componente 1 o PC1 siempre es la dirección donde existe la **mayor varianza**. Si este componente está fuertemente dominado por "velocidad y resistencia", entonces esas variables son los principales descriptores o "diferenciadores" numéricos entre un jugador y otro.

---

## Pregunta 11
Determinar cuales de los siguientes subconjuntos de $\mathbb{R}^{2}$ son conexos bajo la topología estándar. (Elegir todas las respuestas correctas.)  

- [ ] $\{(x,y)\in \mathbb{R}^{2} \mid x^{2}=1\}$
- [x] **$\{(x,y)\in \mathbb{R}^{2} \mid x^{2}=y^{2}\}$**
- [x] **$\{(x,y)\in \mathbb{R}^{2} \mid x^{2}+y^{2}=1\}$**
- [ ] $\{(x,y)\in \mathbb{R}^{2} \mid x^{2}-y^{2}=1\}$

**Explicación:** Un [[Espacio conexo]] es aquel que no puede dividirse en dos piezas disjuntas separadas. $x^2=1$ son dos líneas paralelas separadas; $x^2-y^2=1$ es una hipérbola con dos ramas separadas. Sin embargo, $x^2=y^2$ es una cruz o "X" conectada en el origen, y $x^2+y^2=1$ es un círculo continuo. Por tanto, estos dos últimos son conexos.

---


## Pregunta 12
¿Cuál es la ventaja principal de usar gráficos interactivos en análisis de datos?  

- [ ] General análisis automáticos
- [ ] Reducen el tamaño del conjunto de datos
- [x] **Permiten filtrar y explorar los datos en profundidad**
- [ ] Aumentan la precisión de los modelos predictivos

**Explicación:** En la [[Visualización de datos]], los gráficos dinámicos (usando herramientas como Plotly o Dash) permiten a los usuarios hacer zoom, seleccionar subconjuntos y pasar el cursor para leer valores exactos (`tooltips`), mejorando drásticamente el análisis exploratorio (EDA).

---

## Pregunta 13
¿Cuál de los siguientes gráficos es más útil para visualizar la relación entre dos variables numéricas?  

- [ ] Gráfico de barras
- [ ] Gráfico de pastel
- [x] **Diagrama de dispersión**
- [ ] Histograma

**Explicación:** Al igual que en la pregunta 19, el [[Diagrama de dispersión]] permite situar valores numéricos a lo largo de un eje cartesiano, siendo la representación óptima y nativa para correlacionar dos valores continuos.

---

## Pregunta 14
¿Qué problema se soluciona con la técnica de "one-hot encoding"?  

- [ ] Valores atípicos en los datos
- [ ] Reducción de dimensionalidad
- [x] **Codificación de variables categóricas en valores numéricos**
- [ ] Falta de datos en algunas filas

**Explicación:** El [[One-Hot Encoding]] soluciona el problema de que los algoritmos matemáticos no entienden categorías en texto. Crea múltiples columnas binarias, evitando además asumir un orden jerárquico artificial entre las categorías.

---
