# 📚 Temario y Formulario: Examen Integrador de Ciencia de Datos

Esta es tu guía maestra ("Cheat Sheet") para el examen integrador. Contiene fórmulas matemáticas estructuradas, algoritmos paso a paso y la teoría fundamental extraída de tus 4 sesiones de estudio.

---

## 1. Probabilidad, Estadística e Inferencia

### Medidas Descriptivas
*   **[[Media aritmética]]:** Promedio matemático. **Altamente sensible** a `[[Valores atípicos (Outliers)]]`.
*   **[[Mediana]]:** El punto medio exacto de los datos ordenados. **Robusta** ante atípicos.
*   **[[Varianza]] ($\sigma^2$) y Desviación Estándar ($\sigma$):** Miden la dispersión. Elevan las diferencias al cuadrado, por lo que **se ven muy afectadas por los atípicos**. Si la varianza es 0, todos los datos son idénticos.
*   **[[Rango Intercuartílico (IQR)]]:** Distancia entre Q3 y Q1. Abarca el **50% central** de los datos. Se usa en los `[[Boxplot]]` para detectar atípicos (límites a $1.5 \times IQR$).
*   **[[Sesgo (Asimetría)]]:** 
    *   *Sesgo positivo (a la derecha):* Media > Mediana. Cola larga a la derecha.
    *   *Sesgo negativo (a la izquierda):* Media < Mediana. Cola larga a la izquierda.

### Pruebas de Hipótesis y P-Valor
> [!info] Conceptos Clave
> *   **[[Valor p]]:** Probabilidad de obtener los resultados observados asumiendo que la Hipótesis Nula ($H_0$) es verdadera. Si $p < \alpha$, rechazamos $H_0$.
> *   **[[Nivel de significancia (Alfa)]] ($\alpha$):** El riesgo (ej. 5%) que estamos dispuestos a correr de cometer un Error de Tipo I.
> *   **[[Error de Tipo I]]:** Falso Positivo. Rechazar $H_0$ cuando en realidad era verdadera.
> *   **[[Error de Tipo II]]:** Falso Negativo. No rechazar $H_0$ cuando era falsa.

**¿Qué prueba elegir?**
1.  **[[Prueba T de Student]] (1 muestra):** Comparar la media muestral contra un valor histórico/poblacional conocido.
2.  **[[Prueba T de Student para muestras independientes]]:** Comparar las medias de **solo dos** grupos no relacionados.
3.  **[[ANOVA]]:** Comparar las medias de **tres o más** grupos.
4.  **[[Prueba Chi-Cuadrado]]:** Evaluar la relación/independencia entre dos **variables categóricas**.

### Cadenas de Markov
Para predecir el estado futuro $n$ pasos adelante partiendo de un estado inicial $v_0$, multiplicamos el vector por la matriz de transición $P$ elevada a $n$:
$$ v_n = v_0 \cdot P^n $$

### Teorema de Bayes
$$ P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} $$
> [!example]- Paso a paso: Paradoja del Falso Positivo
> Enfermedad afecta al 1% ($P(E) = 0.01$, por lo tanto sano $P(E')=0.99$). La prueba tiene sensibilidad del 95% ($P(+|E)=0.95$) y especificidad del 95% (tasa de falsos positivos $P(+|E')=0.05$). Si das positivo, ¿cuál es la probabilidad real de estar enfermo?
> 
> 1.  **Calcular el denominador (Probabilidad Total de dar Positivo):** 
>     $P(+) = P(+|E)P(E) + P(+|E')P(E')$
>     $P(+) = (0.95 \cdot 0.01) + (0.05 \cdot 0.99) = 0.0095 + 0.0495 = 0.059$
> 2.  **Calcular numerador y dividir:**
>     $P(E|+) = \frac{0.0095}{0.059} = 0.161 \rightarrow \mathbf{16.1\%}$

---

## 2. Criptoseguridad y Álgebra Modular

### Conceptos Base
*   **Matemática Modular:** $a \equiv b \pmod n$ significa que $a$ y $b$ dejan el mismo residuo al dividirse por $n$.
*   **Inverso Multiplicativo Modular:** El inverso de $A \pmod M$ es un número $X$ tal que $(A \cdot X) \equiv 1 \pmod M$. Se calcula usualmente con el `[[Algoritmo de Euclides Extendido]]`.

### Protocolo Diffie-Hellman (Paso a paso)
> [!tip] Objetivo
> Dos partes (Alice y Bob) generan una llave secreta compartida sobre un canal inseguro sin mandarla explícitamente.

1.  **Acuerdan parámetros públicos:** Un número primo grande $q$ y una raíz primitiva $\alpha$.
2.  **Generan claves privadas (secretas):** Alice elige $X_A$ y Bob elige $X_B$.
3.  **Calculan claves públicas y las intercambian:**
    *   Alice: $Y_A = \alpha^{X_A} \pmod q$
    *   Bob: $Y_B = \alpha^{X_B} \pmod q$
4.  **Generación de la clave compartida ($K$):**
    *   Alice usa la pública de Bob: $K = (Y_B)^{X_A} \pmod q$
    *   Bob usa la pública de Alice: $K = (Y_A)^{X_B} \pmod q$
    *   Ambos llegan a exactamente el mismo número $K$.

### Protocolo ElGamal (Paso a paso)
Es similar a Diffie-Hellman pero usado para **cifrar mensajes**.

1.  **Generación de Claves (Receptor):** Elige primo $q$, raíz $\alpha$, y un privado $X_A$. Su clave pública es $\{q, \alpha, Y_A\}$, donde $Y_A = \alpha^{X_A} \pmod q$.
2.  **Cifrado (Emisor):** Quiere mandar un mensaje $M$. Elige un entero aleatorio $k$.
    *   Calcula clave efímera: $K = (Y_A)^k \pmod q$
    *   Genera el criptograma (C1, C2): 
        $C_1 = \alpha^k \pmod q$
        $C_2 = (K \cdot M) \pmod q$
3.  **Descifrado (Receptor):** Recibe $(C_1, C_2)$.
    *   Recupera $K$: $K = (C_1)^{X_A} \pmod q$
    *   Recupera el mensaje: $M = (C_2 \cdot K^{-1}) \pmod q$

---

## 3. Modelos de Optimización

### Algoritmos Bioinspirados (Metaheurísticas)
*   **[[Algoritmos Genéticos (GA)]]:** Usan selección, cruzamiento (crossover) y mutación.
*   **[[Optimización por Enjambre de Partículas (PSO)]]:** Cada "partícula" ajusta su velocidad y posición basándose en su mejor experiencia individual (`pbest`) y la mejor experiencia de todo el enjambre (`gbest`).
*   **[[Optimización por Colonia de Hormigas (ACO)]]:** Las hormigas dejan **rastros de feromonas** que se evaporan con el tiempo. Los caminos más cortos concentran más feromonas, atrayendo a más hormigas.

> [!warning] Exploración vs Explotación
> *   **Exploración:** Buscar en áreas nuevas y desconocidas del espacio de soluciones (evita quedar atrapado en óptimos locales).
> *   **Explotación:** Refinar y buscar minuciosamente alrededor de una buena solución ya encontrada.

### Modelos de Redes (IO)
*   **[[Problema de Asignación]]:** La restricción principal es que **cada tarea se asigna a exactamente un recurso**, y las variables son binarias ($x_{ij} \in \{0,1\}$).
*   **[[Problema de Transporte]]:** Las sumas de las cantidades enviadas desde un origen no pueden superar su **Oferta**, y deben satisfacer estrictamente la **Demanda** de los destinos.

---

## 4. Topología y Series de Tiempo (Ciencia de Datos)

### Topología y TDA
*   **[[Conjunto cerrado]]:** Contiene todos sus límites (ej. $[0, 1]$ o $[0, \infty)$).
*   **[[Espacio conexo]]:** No está partido en piezas. Una cruz $x^2=y^2$ o un círculo $x^2+y^2=1$ son conexos.
*   **[[Números de Betti]] ($b_0, b_1, b_2$):**
    *   $b_0$: Número de componentes conectados.
    *   $b_1$: Número de lazos / túneles (agujeros 1D).
    *   $b_2$: Número de huecos o cavidades (volumen atrapado 2D).
    *   *Toro:* $(1, 2, 1)$. *Esfera:* $(1, 0, 1)$.
*   **[[Análisis Topológico de Datos (TDA)]]:** Usa una **filtración** para ver cómo nacen y mueren las características topológicas a distintas escalas (Homología Persistente), encontrando estructuras inmunes al ruido.

### Series de Tiempo
*   **[[Estacionariedad]]:** Es un requisito **estricto** antes de aplicar ARIMA. Significa que la media y la varianza no cambian con el tiempo.
*   **[[ARIMA]]:** No soporta estacionalidad pura. Requiere revisar la ACF (para inferir "q") y la **[[Autocorrelación parcial (PACF)]]** (para inferir "p").
*   **[[SARIMA]]:** La extensión natural que maneja patrones cíclicos/estacionales.

### Análisis de Componentes Principales (PCA)
*   **Propósito:** `[[Reducción de dimensionalidad]]` conservando la máxima información posible.
*   **Mecanismo:** Encuentra los `[[Eigenvectores]]` (direcciones) de la matriz de covarianza. El PC1 captura la **mayor varianza**.

---

## 5. Inteligencia Artificial y Deep Learning

### Evaluación de Clasificadores (Métricas)
> [!warning] Casos de Clases Desbalanceadas
> **NUNCA uses Accuracy (Exactitud).** En medicina (ej. buscar hepatitis), un 99% de pacientes están sanos. Si el modelo dice "todos sanos", tiene 99% de Accuracy pero es inútil.

*   **[[Falsos Positivos (FP)]]:** Decir que alguien está enfermo cuando está sano. (Generalmente aceptable, requiere más pruebas).
*   **[[Falsos Negativos (FN)]]:** Decir que alguien está sano cuando está enfermo. **(Muy peligroso, falta de tratamiento).**
*   **[[Recall (Sensibilidad)]]:** Mide qué porcentaje de los enfermos reales logró encontrar el modelo. **Se usa para minimizar Falsos Negativos.**
*   **[[Precision]]:** De los que el modelo dijo que estaban enfermos, ¿cuántos realmente lo estaban? **Se usa para minimizar Falsos Positivos.**

### Arquitectura de CNN (Visión por Computadora)
*   **[[Convolución]]:** Aplica un `[[Kernel]]` (filtro) deslizable para extraer patrones espaciales (bordes, formas).
*   **[[Capa de Pooling (Submuestreo)]]:** Reduce la dimensionalidad espacial manteniendo la información más importante (ej. Max-pooling).
*   **[[Imágenes en Escala de grises]]:** Tienen un solo canal donde los píxeles indican intensidad de luz (0-255).

### Deep Learning General
*   **[[Backpropagation (Retropropagación)]]:** El algoritmo usado para ajustar los pesos propagando el gradiente de error hacia atrás.
*   **[[Stochastic Gradient Descent (SGD)]]:** Optimizador común. Si la **Tasa de Aprendizaje (Learning Rate)** es muy alta, el modelo "oscilará" y no convergerá.
*   **[[Overfitting]] (Sobreajuste):** Memorizar los datos en lugar de generalizar. Se combate con **[[Dropout]]** y **Regularización**.
*   **[[ReLU]]:** Función de activación $f(x) = \max(0, x)$. Devuelve el valor si es positivo, o 0 si es negativo.
*   **[[Softmax]]:** Se usa siempre en la **capa de salida** de problemas de clasificación multiclase para generar probabilidades que sumen 1.0.
*   **[[Transfer Learning (Transferencia de aprendizaje)]]:** Usar pesos pre-entrenados en grandes volúmenes de datos (`Pre-training`) y ajustarlos a tu problema específico (`Fine-tuning`).

---
*Documento generado consolidando las Sesiones 1, 2, 3 y 4 del material de Examen Integrador.*
