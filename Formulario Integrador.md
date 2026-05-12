# 📚 Formulario y Temario Exhaustivo: Examen Integrador

Esta es tu guía maestra definitiva. Contiene la **teoría completa** y la **práctica paso a paso** para absolutamente todos los conceptos, preguntas y ejercicios abordados en las 4 sesiones de tu examen de Ingeniería en Ciencias de Datos.

---

## 1. Probabilidad, Estadística y Regresión (Sesión 1)

### 1.1 Estadística Descriptiva
*   **[[Media aritmética]]:** $\bar{x} = \frac{1}{n}\sum x_i$. **Altamente sensible** a [[Valores atípicos (Outliers)]].
*   **[[Mediana]]:** El punto medio exacto. **Robusta** ante atípicos.
*   **[[Varianza]] ($\sigma^2$):** $\frac{\sum (x_i - \bar{x})^2}{n}$. Mide dispersión cuadrática. Si es 0, todos los datos son iguales.
*   **[[Rango Intercuartílico (IQR)]]:** $IQR = Q3 - Q1$. Se usa en el [[Boxplot]]. Límite superior: $Q3 + 1.5(IQR)$.
*   **[[Correlación]]:** Relación lineal entre dos variables (Pearson). **Ojo:** *Correlación no implica causalidad.*

### 1.2 Modelos de Regresión
*   **[[Regresión Lineal Simple]]:** $Y = \beta_0 + \beta_1 X$. Predice una variable continua basándose en 1 predictora.
*   **[[Regresión Lineal Múltiple]]:** $Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 \dots$ Predice basándose en $n$ variables.
*   **[[Regresión Logística]]:** Usada para **Clasificación Binaria** (ej. Sí/No, 1/0). Usa la función Logit/Sigmoide para estimar la probabilidad de que algo pertenezca a la clase 1.
*   **[[R-cuadrado ($R^2$)]]:** Mide el porcentaje de la varianza de $Y$ que el modelo logra explicar.

### 1.3 Distribuciones de Probabilidad (Práctica)
*   **[[Distribución de Poisson]]:** Modela cantidad de eventos en un intervalo de tiempo o espacio.
    $$ P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!} $$
    *Práctica:* Si un call center recibe un promedio de $\lambda = 3$ llamadas por hora, la probabilidad de recibir $k=2$ llamadas en una hora es: $\frac{3^2 \cdot e^{-3}}{2!} = \frac{9 \cdot 0.0497}{2} \approx 0.224$.
*   **[[Distribución Normal]]:** Campana de Gauss simétrica. Regla empírica 68-95-99.7.
*   **[[Distribución Exponencial]]:** Modela el tiempo de espera hasta que ocurra un evento de Poisson.

### 1.4 Pruebas de Hipótesis y P-Valor
*   **[[Valor p]]:** Probabilidad de obtener tus resultados si la Hipótesis Nula ($H_0$) fuera real. Si $p < 0.05$ (Nivel de significancia $\alpha$), rechazas $H_0$.
*   **[[Prueba T de Student]]:** Para comparar las medias de **dos grupos** o 1 grupo vs un número.
*   **[[ANOVA]]:** Prueba $F$ para comparar las medias de **tres o más grupos**.
*   **[[Prueba Chi-Cuadrado]]:** Para relación de independencia entre **variables categóricas**.

### 1.5 Cadenas de Markov (Práctica)
Una **[[Matriz de transición]]** $P$ describe las probabilidades de pasar de un estado a otro (ej. $S_1 \rightarrow S_2$). **Condición matemática:** La suma de probabilidades de cada fila en la matriz debe ser **exactamente 1**.
*   **Ecuación de estado futuro:** Para predecir el estado en el paso $n$, partiendo de un vector inicial $v_0$: $$ v_n = v_0 \cdot P^n $$

> [!example]- Ejercicio de Práctica: Estados $S_1, S_2, S_3$
> Asume un sistema con 3 estados ($S_1, S_2, S_3$) y la siguiente matriz de transición $P$:
> $$ P = \begin{bmatrix} 0.5 & 0.3 & 0.2 \\ 0.1 & 0.6 & 0.3 \\ 0.0 & 0.4 & 0.6 \end{bmatrix} $$
> Si inicialmente estamos 100% seguros de estar en el estado $S_1$, nuestro vector inicial es $v_0 = [1, 0, 0]$.
> ¿Cuál será la probabilidad de estar en cada estado en el paso 1 ($v_1$)?
> $v_1 = v_0 \cdot P = [1, 0, 0] \cdot \begin{bmatrix} 0.5 & 0.3 & 0.2 \\ 0.1 & 0.6 & 0.3 \\ 0.0 & 0.4 & 0.6 \end{bmatrix} = [0.5, 0.3, 0.2]$
> En el paso 1, hay un 50% de probabilidad de seguir en $S_1$, 30% de ir a $S_2$, y 20% a $S_3$.
> ¿Y para el paso 2 ($v_2$)? Multiplicas el vector $v_1$ por $P$ nuevamente:
> $v_2 = [0.5, 0.3, 0.2] \cdot P = [0.28, 0.41, 0.31]$.

---

## 2. Criptoseguridad y Álgebra Modular (Sesión 2)

### 2.1 Aritmética Modular (Práctica)
*   **Congruencia:** $a \equiv b \pmod n$ significa que el residuo es el mismo al dividir entre $n$.
*   **Inverso Multiplicativo Modular:** Buscar un número $X$ tal que $(A \cdot X) \equiv 1 \pmod M$.

> [!example]- Práctica: Inverso con Algoritmo de Euclides Extendido
> Queremos encontrar el inverso multiplicativo de **$17 \pmod{26}$**. Es decir, qué valor $X$ cumple: $17X \equiv 1 \pmod{26}$.
> 
> Se resuelve planteando divisiones sucesivas entre el módulo (26) y el número (17), quedándonos con los residuos:
> 1.  $26 = 17(1) + 9$  **(Residuo = 9)**
> 2.  $17 = 9(1) + 8$  **(Residuo = 8)**
> 3.  $9 = 8(1) + 1$    **(¡Llegamos al residuo 1!)**
> 
> Ahora "despejamos" de abajo hacia arriba (Euclides Extendido) para expresar el residuo 1 en función del 17 y el 26:
> *   De (3): $1 = 9 - 8(1)$
> *   De (2), sabemos que $8 = 17 - 9(1)$. Sustituimos el 8 en la ecuación anterior:
>     $1 = 9 - (17 - 9(1)) \Rightarrow 1 = 2(9) - 17$
> *   De (1), sabemos que $9 = 26 - 17(1)$. Sustituimos el 9 en la ecuación anterior:
>     $1 = 2(26 - 17) - 17 \Rightarrow 1 = 2(26) - 3(17)$
> 
> Como estamos trabajando en Módulo 26, el término $2(26)$ se vuelve $0$. 
> Nos queda: $1 \equiv -3(17) \pmod{26}$.
> Por lo tanto, el inverso es **-3**. Para hacerlo positivo en el mundo modular, le sumamos el módulo: $-3 + 26 = \mathbf{23}$.
> **Respuesta:** El inverso multiplicativo de $17 \pmod{26}$ es **23**.

### 2.2 Protocolo Diffie-Hellman (Práctica Completa)
*Teoría:* Algoritmo de clave asimétrica cuyo único propósito es **generar una clave secreta compartida ($K$)** en un canal interceptado, sin transmitir jamás dicha clave.

*   **Práctica Paso a Paso:**
    1.  **Público:** Primo $p = 23$, Raíz base $g = 5$.
    2.  **Privado:** Alice elige secreto $a = 6$, Bob elige $b = 15$.
    3.  **Cálculo Público:**
        *   Alice manda $A = 5^6 \pmod{23} = 8$.
        *   Bob manda $B = 5^{15} \pmod{23} = 19$.
    4.  **Generación de Llave Compartida ($K$):**
        *   Alice hace $K = B^a \pmod{23} = 19^6 \pmod{23} = 2$.
        *   Bob hace $K = A^b \pmod{23} = 8^{15} \pmod{23} = 2$. **El secreto es 2.**

### 2.3 Protocolo ElGamal y ECC
*   **ElGamal:** Usa la misma matemática de logaritmos discretos que Diffie-Hellman, pero se usa para **Cifrar mensajes**. Alice genera una llave efímera, cifra el mensaje $M$ multiplicándolo, y Bob lo recupera dividiendo (con su inverso modular).
*   **[[Criptografía de Curva Elíptica (ECC)]]:** *Teoría:* Alternativa moderna a RSA. Ofrece la misma seguridad criptográfica que algoritmos antiguos pero con **tamaños de clave drásticamente más pequeños**, lo que la hace ideal para dispositivos rápidos.

---

## 3. Modelos de Optimización (Sesión 2)

### 3.1 Modelos de Redes Matemáticos
*   **[[Problema de Asignación]]:** Emparejamiento perfecto (ej. 5 taxis para 5 clientes minimizando distancia). Usa variables **Binarias** $x_{ij} \in \{0,1\}$. Restricción: Suma de la fila $= 1$, suma de columna $= 1$.
*   **[[Problema de Transporte]]:** Llevar producto de fábricas a tiendas minimizando costo de envío. Variables **Continuas**. Restricciones: Suma de envíos $\le$ Oferta, suma de llegadas $=$ Demanda.

### 3.2 Metaheurísticas y Bioinspiración
*   **Dilema Crítico:** 
    *   **Exploración:** Saltar a rincones lejanos del espacio de búsqueda para no estancarse.
    *   **Explotación:** Refinar una solución local que ya vimos que es buena.
*   **[[Algoritmos Genéticos (GA)]]:** Usan una **Población** inicial. Las mejores soluciones sobreviven (Selección por *fitness*), se combinan (`Crossover`) y a veces mutan aleatoriamente (`Mutación` $\rightarrow$ inducción de Exploración).
*   **[[Optimización por Enjambre de Partículas (PSO)]]:** Cada "partícula" tiene velocidad. Decide hacia dónde volar basándose en su memoria personal (`pbest`), la memoria colectiva (`gbest`) y su inercia.
*   **[[Colonia de Hormigas (ACO)]]:** Diseñado para grafos. Las hormigas dejan rastro de **feromonas** que se evapora. Rutas cortas acumulan feromonas rápido, atrayendo a toda la colonia.

---

## 4. Topología y Pandas (Sesión 3)

### 4.1 Preparación de Datos (Pandas)
*   **DataFrames:** Tablas estructuradas. Operaciones vitales de limpieza incluyen manejo de nulos (`dropna`, `fillna`).
*   **Tipos de Join (Cruces):**
    *   `Inner Join`: Solo la intersección (lo que existe en A y en B).
    *   `Left Join`: Todo lo de A, y lo que coincida de B. Nulos si B no tiene.
    *   `Outer Join`: Une absolutamente todo, muchísimos valores nulos (NaN).

### 4.2 Topología y TDA
*   **[[Espacio conexo]]:** No está separado. (Un círculo es conexo; una hipérbola de dos curvas no lo es).
*   **[[Números de Betti]] ($b_0, b_1, b_2$):**
    *   $b_0$: Cantidad de fragmentos aislados.
    *   $b_1$: Número de lazos / túneles (agujeros que atraviesan, como en una dona).
    *   $b_2$: Número de huecos / cavidades internas (como el aire dentro de un globo).
*   **[[Análisis Topológico de Datos (TDA)]]:** Transforma nubes de puntos en figuras topológicas mediante **Filtración** (engordando los puntos por radio) para buscar "Homología Persistente" (hoyos que duran mucho = la forma real de los datos).

### 4.3 Reducción: PCA
*   **[[Análisis de Componentes Principales (PCA)]]:** Reduce muchas columnas a pocas, conservando varianza. **Práctica:** Se requiere estandarizar datos siempre. El PC1 (Eigenvector principal) es la línea que cruza el clúster conservando la mayor separación matemática de los datos.

### 4.4 Series de Tiempo
*   **[[Estacionariedad]]:** *Requisito absoluto.* Media y varianza deben ser constantes. Si hay tendencia, debes aplicar *diferenciación*.
*   **[[ARIMA]] ($p, d, q$):** 
    *   $p$ (Auto-Regresivo): Se lee de la gráfica **[[PACF]]** (Autocorrelación Parcial).
    *   $d$ (Diferenciación): Cuántas veces restaste la serie para hacerla estacionaria.
    *   $q$ (Media Móvil): Se lee de la gráfica **[[ACF]]** (Autocorrelación).
*   **[[SARIMA]]:** Añade el componente estacional $S$ (para ventas cíclicas en Diciembre, por ejemplo).

---

## 5. Inteligencia Artificial (Sesión 4)

### 5.1 Probabilidad Bayesiana (Teoría y Práctica)
*   **Teoría:** Ajustar la probabilidad de una Hipótesis (Distribución a priori) con nueva evidencia para obtener la **Distribución Posterior**.
$$ P(H|D) = \frac{P(D|H) \cdot P(H)}{P(D)} $$

> [!example]- Práctica Exhaustiva: Paradoja Médica
> Enfermedad: 1% población ($P(E) = 0.01$, Sano $P(S) = 0.99$).
> Prueba: Sensibilidad 99% ($P(+|E) = 0.99$), Especificidad 99% (Falsos positivos $P(+|S) = 0.01$).
> Si das positivo, probabilidad de enfermo:
> $P(+) = (0.99 \cdot 0.01) + (0.01 \cdot 0.99) = 0.0099 + 0.0099 = 0.0198$ (Probabilidad total).
> $P(E|+) = \frac{0.0099}{0.0198} = \mathbf{0.5 \text{ (50\%)}}.$ ¡A pesar del 99% de eficacia, solo hay 50% de probabilidad real por la rareza de la enfermedad!

### 5.2 Deep Learning (Entrenamiento)
*   **Arquitectura:** Redes multicapa interconectadas. Un GPU es vital por el paralelismo tensorial.
*   **[[Backpropagation]]:** Aplica la regla de la cadena del cálculo para devolver el gradiente de error desde la salida a la entrada, indicando cómo ajustar los pesos.
*   **[[SGD]] (Stochastic Gradient Descent):** El optimizador.
    *   **Tasa de Aprendizaje:** Si es muy grande $\rightarrow$ Rebota / Oscila. Si es muy pequeña $\rightarrow$ Tarda años.
*   **[[Overfitting]]:** El modelo se aprende de memoria el training set. *Solución:* Regularización L1/L2 o **[[Dropout]]** (apagar neuronas temporalmente).
*   **Funciones de Activación:**
    *   `[[ReLU]]`: $\max(0, x)$. Corta los negativos, deja los positivos. Estándar para capas ocultas.
    *   `[[Softmax]]`: Estándar para la **capa final** en clasificación múltiple. Convierte la salida en probabilidades sumadas a 1.0.

### 5.3 Redes Convolucionales (CNN)
*   Ideal para **Imágenes** y datos de cuadrícula espacial.
*   **[[Convolución]]:** Un `Kernel` (matriz pequeña de filtro) escanea la imagen localmente detectando bordes, texturas y formas.
*   **[[Pooling]] (Submuestreo):** (Ej. Max-Pooling). Reduce la escala espacial (resolución de la matriz) conservando solo la activación máxima. Esto la hace invariante a si un objeto se movió un par de píxeles.

### 5.4 Métricas de Evaluación
> [!warning] El Problema de Clases Desbalanceadas
> Si un banco tiene 99% transacciones normales y 1% fraudes, un modelo inútil que diga "todo es normal" tiene **99% de Accuracy**. ¡Nunca uses Accuracy aquí!

*   **Matriz de Confusión:** 
    *   Verdadero Positivo (TP), Verdadero Negativo (TN).
    *   Falso Positivo (FP) = Falsa alarma.
    *   Falso Negativo (FN) = Enfermo detectado como sano. **(El peor escenario médico).**
*   **[[Recall]] (Sensibilidad):** $\frac{TP}{TP + FN}$. % de enfermos totales que pudimos rescatar. **Úsalo si tu prioridad absoluta es reducir Falsos Negativos**.
*   **[[Precision]]:** $\frac{TP}{TP + FP}$. % de nuestras alarmas que fueron reales. **Úsalo si tu prioridad es reducir Falsos Positivos.**
*   **[[F1-Score]]:** Media armónica para lograr un equilibrio perfecto entre Precision y Recall.
