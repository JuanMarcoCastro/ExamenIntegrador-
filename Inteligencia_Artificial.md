# 📚 Banco de Preguntas: Tema Inteligencia Artificial

## Pregunta 1
¿Qué es una imagen en escala de grises?  

- [ ] Una imagen con múltiples canales de color.
- [ ] Una imagen con solo dos colores.
- [ ] Una imagen con solo un color predominante.
- [x] **Una imagen con valores de píxeles que representan intensidad de luz.**

**Explicación:** En [[Procesamiento de imágenes]], una imagen en escala de grises tiene un solo canal. En lugar de colores, cada [[Píxel]] almacena un valor numérico (generalmente entre 0 y 255) que representa exclusivamente su luminancia o intensidad de luz, desde negro puro (0) hasta blanco puro (255).

---

## Pregunta 2
¿Qué significa aplicar un filtro convolucional en procesamiento de imágenes?  

- [ ] Reducir la resolución de la imagen.
- [ ] Transformar la imagen en texto.
- [x] **Aplicar un kernel para extraer características específicas.**
- [ ] Aumentar el tamaño de la imagen.

**Explicación:** Una [[Convolución]] es una operación matemática donde una pequeña matriz llamada filtro o [[Kernel]] se desliza sobre la imagen para transformarla, permitiendo extraer características espaciales como desenfoques, realce o detección de bordes.

---

## Pregunta 3
¿Cuál de las siguientes técnicas se utiliza para reducir el ruido en una imagen digital?  

- [ ] Convolución.
- [ ] Max-pooling.
- [x] **Filtro de suavizado (blur).**
- [ ] Normalización de datos.

**Explicación:** Los filtros de suavizado, como el desenfoque gaussiano ([[Filtro Gaussiano]]), promedian los píxeles adyacentes, lo cual difumina transiciones abruptas y es sumamente eficaz para atenuar o reducir el ruido de alta frecuencia en una imagen.

---

## Pregunta 4
¿Cuál de las siguientes afirmaciones es correcta sobre las CNN?  

- [ ] No requieren ajuste de pesos durante el entrenamiento.
- [ ] Solo funcionan con imágenes en color.
- [ ] No pueden manejar imágenes en escala de grises.
- [x] **Utilizan convoluciones para detectar características espaciales en los datos.**

**Explicación:** Las `[[Redes Neuronales Convolucionales (CNN)]]` son arquitecturas de Deep Learning diseñadas específicamente para procesar datos con topología de cuadrícula (como imágenes), usando capas convolucionales para aprender jerarquías de características espaciales locales.

---

## Pregunta 5
¿Qué componente clave de una CNN permite reducir la dimensionalidad de las imágenes mientras mantiene características relevantes?  

- [ ] Retropropagación.
- [ ] Capa de convolución.
- [x] **Capa de pooling.**
- [ ] Función de activación.

**Explicación:** La `[[Capa de Pooling (Submuestreo)]]` (como Max-Pooling o Average-Pooling) resume regiones vecinas en un solo valor. Esto reduce drásticamente las dimensiones espaciales y la carga computacional, logrando invarianza a pequeñas traslaciones.

---

## Pregunta 6
¿Qué técnica se utiliza en las CNN para detectar patrones locales en imágenes, como bordes o formas?  

- [ ] Normalización.
- [ ] Max-pooling.
- [ ] Regularización.
- [x] **Convolución.**

**Explicación:** Al aplicar múltiples filtros en la `[[Capa Convolucional]]`, la red escanea parches locales de la imagen para identificar patrones. Las primeras capas aprenden a detectar bordes simples, y las capas más profundas aprenden a combinar esos bordes para detectar formas complejas.

---

## Pregunta 7
Asume que tienes un clasificador binario que se entrenó con un conjunto de datos en el que el número de elementos de la clase positiva es mucho menor al de la clase negativa. De las siguientes métricas, ¿cuál sería la métrica que **no** es recomendable para evaluar el rendimiento del clasificador?  

- [ ] "Recall"
- [ ] "Precision"
- [x] **"Accuracy".**
- [ ] "F1-Score"

**Explicación:** En problemas de `[[Clases Desbalanceadas]]`, la Exactitud (`[[Accuracy]]`) es engañosa. Si el 99% de los datos son clase negativa, un modelo inútil que siempre prediga "negativo" tendrá un 99% de Accuracy sin haber aprendido a identificar ningún positivo.

---

## Pregunta 8
Asume que tenemos un conjunto de entrenamiento en el que las clases no están balanceadas. Si estamos interesados en reducir la cantidad de falsos negativos, ¿cuál de las siguientes métricas sería la más relevante para evaluar qué tan bien está funcionando el clasificador binario?  

- [x] **Recall**
- [ ] F1-score
- [ ] Accuracy
- [ ] Precision

**Explicación:** El `[[Recall (Sensibilidad)]]` responde a la pregunta: "De todos los positivos reales que existen, ¿cuántos logró encontrar mi modelo?". Por definición, maximizar el Recall minimiza matemáticamente la cantidad de `[[Falsos Negativos]]`.

---

## Pregunta 9
Se quiere implementar un clasificador binario para la detección de hepatitis. En este escenario, ¿son preferibles los falsos positivos o los falsos negativos? Asume que la categoría positiva es tener la enfermedad.  

- [x] **Falsos positivos.**
- [ ] Falsos negativos.
- [ ] Ambos son graves.

**Explicación:** En medicina, un diagnóstico con `[[Falsos Positivos]]` resulta en hacerle más pruebas a alguien sano (molesto, pero no fatal). Sin embargo, un falso negativo significa decirle a una persona enferma que está sana, dejándola sin tratamiento médico, lo cual es de gravedad crítica.

---

## Pregunta 10
Se quiere implementar un clasificador binario para la detección de hepatitis. En este escenario, ¿es apropiado evaluar el modelo usando "precision" o "recall"? Asume que la categoría positiva es tener la enfermedad.  

- [x] **"Recall".**
- [ ] Ambas métricas son apropiadas.
- [ ] "Precision".

**Explicación:** Al igual que en la pregunta anterior, como queremos evitar a toda costa dejar enfermos sin detectar (falsos negativos), nuestra métrica reina a optimizar debe ser el `[[Recall (Sensibilidad)]]`.

---

## Pregunta 11
¿Qué tipo de hardware suele ser más adecuado para entrenar modelos de aprendizaje profundo?  

- [x] **GPU (Unidad de Procesamiento Gráfico).**
- [ ] Memoria RAM extendida.
- [ ] CPU estándar.
- [ ] SSD de alta velocidad.

**Explicación:** El `[[Deep Learning]]` depende de realizar millones de multiplicaciones de matrices y sumas de forma paralela. Las `[[GPU]]` tienen miles de núcleos pequeños diseñados exactamente para procesar gráficos en paralelo, haciéndolas ideales para el cálculo tensorial.

---

## Pregunta 12
¿Qué característica define al aprendizaje profundo (Deep Learning)?  

- [ ] La eliminación del entrenamiento supervisado.
- [ ] El uso exclusivo de datos estructurados.
- [x] **La implementación de redes neuronales con múltiples capas ocultas.**
- [ ] El uso de algoritmos bayesianos.

**Explicación:** El término "profundo" (`[[Deep Learning]]`) proviene literalmente de la profundidad arquitectónica del modelo. A diferencia de un Perceptrón multicapa simple, usa una cantidad masiva de capas ocultas interconectadas para construir abstracciones complejas.

---

## Pregunta 13
¿Qué técnica es fundamental para evitar el sobreajuste (overfitting) en una red neuronal?  

- [ ] Usar más capas ocultas.
- [ ] Aumentar el tamaño del lote de datos (batch size).
- [ ] Reducir la cantidad de datos.
- [x] **Aplicar regularización o dropout.**

**Explicación:** El `[[Dropout]]` (apagar neuronas aleatoriamente durante el entrenamiento) y las técnicas de `[[Regularización (L1/L2)]]` penalizan la complejidad del modelo, obligándolo a aprender características generales en lugar de "memorizar" el set de entrenamiento (`[[Overfitting]]`).

---

## Pregunta 14
¿Qué ventaja ofrece el uso de redes neuronales profundas en comparación con redes neuronales simples?  

- [ ] Eliminar la necesidad de preprocesamiento de datos.
- [ ] Entrenamiento más rápido.
- [ ] Reducción del costo computacional.
- [x] **Capacidad para aprender características complejas y abstractas.**

**Explicación:** Mientras más capas tiene una `[[Red Neuronal Artificial (ANN)]]`, su representación se vuelve más abstracta jerárquicamente. Por ejemplo: Capa 1 aprende líneas, Capa 2 aprende curvas, Capa 3 aprende ojos, Capa N aprende rostros completos.

---

## Pregunta 15
¿Qué componente de una red neuronal es responsable de ajustar los pesos durante el entrenamiento?  

- [x] **Algoritmo de retropropagación.**
- [ ] Neurona de entrada.
- [ ] Función de pérdida.
- [ ] Función de activación.

**Explicación:** El algoritmo de `[[Backpropagation (Retropropagación)]]` calcula los gradientes de error usando la regla de la cadena del cálculo diferencial, permitiendo que el optimizador (como Adam o SGD) empuje los pesos en la dirección que minimiza la función de pérdida.

---

## Pregunta 16
¿Cuál de los siguientes es un problema común en redes neuronales totalmente conectadas?  

- [x] **Sobreajuste ("overfitting").**
- [ ] Falta de conexión entre capas.
- [ ] Regresión lineal.
- [ ] Subajuste ("underfitting").

**Explicación:** Las capas densas o `[[Redes Fully Connected (FCN)]]` tienen una inmensa cantidad de parámetros porque cada neurona conecta con todas las demás. Este exceso de capacidad las hace sumamente propensas al `[[Overfitting]]` si no se aplica regularización.

---

## Pregunta 17
¿Qué representa la función de activación ReLU (Rectified Linear Unit)?  

- [ ] Una función que aplica una transformación logarítmica a la entrada.
- [x] **Una función que devuelve el valor de entrada si es positivo y 0 si es negativo.**
- [ ] Una función que siempre devuelve valores negativos.
- [ ] Una función que genera un valor binario entre 0 y 1.

**Explicación:** Matemáticamente, `[[ReLU]]` se define como $f(x) = \max(0, x)$. Introduce la no linealidad necesaria para aprender relaciones complejas sin sufrir fuertemente del problema del desvanecimiento del gradiente.

---

## Pregunta 18
¿Qué método es comúnmente utilizado en el entrenamiento de redes neuronales?  

- [ ] Algoritmo de Newton-Raphson.
- [ ] Método simplex.
- [ ] Algoritmo de k-medias.
- [x] **Gradiente descendente estocástico (SGD).**

**Explicación:** El optimizador `[[Stochastic Gradient Descent (SGD)]]` calcula iterativamente la dirección más rápida para bajar por la montaña de la función de coste (gradiente) usando pequeños lotes de datos, ajustando eficientemente los pesos en redes neuronales.

---

## Pregunta 19
En un algoritmo de detección de spam, el 80% de los correos electrónicos de spam contienen la palabra "gratis", mientras que el 15% de los correos electrónicos que no son spam contienen la palabra "gratis". Si el 30% de los correos electrónicos son spam, ¿cuál es la probabilidad de que un correo electrónico que contiene la palabra "gratis" sea spam?  

- [x] **0.696**
- [ ] 0.65
- [ ] 0.642
- [ ] 0.7

**Explicación:** Aplicando el `[[Teorema de Bayes]]`:
$P(\text{Spam} \mid \text{Gratis}) = \frac{P(\text{Gratis} \mid \text{Spam}) \times P(\text{Spam})}{P(\text{Gratis})}$
Donde $P(\text{Gratis}) = (0.80 \times 0.30) + (0.15 \times 0.70) = 0.24 + 0.105 = 0.345$.
Sustituyendo: $\frac{0.24}{0.345} = 0.69565 \dots \approx 0.696$.

---

## Pregunta 20
Una determinada enfermedad afecta al 1% de la población. Una prueba para detectar la enfermedad tiene una sensibilidad del 99% (tasa de verdaderos positivos). Si una persona da positivo, ¿cuál es la probabilidad de que realmente tenga la enfermedad?  

- [ ] 0.9
- [ ] 0.01
- [x] **0.5**
- [ ] 0.55

**Explicación:** Nuevamente con el `[[Teorema de Bayes]]`, asumiendo Sensibilidad y Especificidad del 99% (tasa de falsos positivos 1%):
$P(\text{Enfermo} \mid \text{Positivo}) = \frac{(0.99 \times 0.01)}{(0.99 \times 0.01) + (0.01 \times 0.99)}$
$= \frac{0.0099}{0.0099 + 0.0099} = \frac{0.0099}{0.0198} = 0.5$. Es un efecto clásico de la `[[Paradoja del falso positivo]]` en enfermedades muy raras.

---

## Pregunta 21
¿Para cuál de las siguientes tareas es más adecuada una Red Neuronal Convolucional (CNN)?  

- [ ] Predicción de series temporales.
- [ ] Cálculo de probabilidades.
- [ ] Análisis de texto.
- [x] **Clasificación de imágenes.**

**Explicación:** Las `[[Redes Neuronales Convolucionales (CNN)]]` fueron diseñadas bioinspiradas en la corteza visual animal. Su arquitectura (convolución y pooling) es el estándar de oro (estado del arte) para tareas de `[[Visión por computadora]]` como la clasificación, segmentación y detección de objetos en imágenes.

---

## Pregunta 22
¿Cuál de las siguientes técnicas se utiliza comúnmente en el aprendizaje profundo para manejar grandes volúmenes de datos etiquetados?  

- [ ] Regularización.
- [ ] Reducción de la dimensionalidad.
- [ ] Aplicación de funciones de activación lineales.
- [x] **Preentrenamiento (Pre-training) y ajuste fino (Fine-tuning).**

**Explicación:** El concepto de `[[Transfer Learning (Transferencia de aprendizaje)]]` consiste en tomar una red que ya fue pre-entrenada con millones de imágenes (Pre-training en ImageNet, por ejemplo) y hacerle un "ajuste fino" (Fine-tuning) con tu propio conjunto de datos, ahorrando meses de cómputo y logrando mejor precisión.

---

## Pregunta 23
¿Cuál es el efecto de utilizar una tasa de aprendizaje demasiado alta al entrenar una red neuronal?  

- [ ] El modelo convergerá rápidamente a una solución óptima.
- [x] **El modelo puede oscilar o no converger a una solución óptima.**
- [ ] El modelo estará menos propenso al sobreajuste.
- [ ] El modelo se entrenará demasiado lento.

**Explicación:** La `[[Tasa de aprendizaje (Learning rate)]]` dicta el tamaño del paso que da el optimizador. Si es muy baja, el modelo tarda años en entrenar. Si es demasiado alta, el optimizador dará saltos enormes cruzando el valle del mínimo global repetidas veces, rebotando ("oscilando") y fallando en converger.

---


## Pregunta 24
¿Cuál es uno de los principales desafíos del aprendizaje profundo?  

- [ ] Es más fácil de interpretar que los modelos tradicionales.
- [ ] No puede manejar datos no estructurados.
- [ ] No permite la automatización de tareas.
- [x] **Requiere grandes cantidades de datos y poder computacional.**

**Explicación:** A diferencia del Machine Learning tradicional, las arquitecturas de redes profundas necesitan miles o millones de observaciones etiquetadas ([[Big Data]]) y horas/días de entrenamiento en hardware especializado ([[GPU]]) para converger adecuadamente.

---

