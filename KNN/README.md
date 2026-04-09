# example-KNN
Estudio de aplicación de KNN y de la selección de hiperparámetros del modelo

## Fundamentos teóricos

¿Qué es KNN y cómo funciona? (lógica de vecinos más cercanos)
KNN para clasificación vs. KNN para regresión
Supuestos del algoritmo (lazy learner, no paramétrico)
La "maldición de la dimensionalidad"


### Métricas de distancia

Distancia Euclidiana
Distancia Manhattan
Distancia Minkowski (generalización de las anteriores)
Distancia de Hamming (para datos categóricos)
Distancia coseno (para texto/vectores)
¿Cuándo usar cada una?


### Hiperparámetro K

Cómo elegir el valor de K
Efecto de K bajo (overfitting) vs. K alto (underfitting)
Uso de validación cruzada para encontrar el K óptimo
K par vs. impar en clasificación binaria


### Preprocesamiento de datos

Escalado de features (StandardScaler, MinMaxScaler) — crítico en KNN
Codificación de variables categóricas (One-Hot, Label Encoding)
Manejo de valores nulos
Reducción de dimensionalidad (PCA, t-SNE) para mitigar la maldición dimensional


### KNN ponderado

Voto ponderado por distancia (vecinos más cercanos pesan más)
Comparación con KNN uniforme
Cuándo conviene usar pesos


### Evaluación del modelo

Métricas de clasificación: Accuracy, Precision, Recall, F1, ROC-AUC
Métricas de regresión: MAE, MSE, RMSE, R²
Matriz de confusión
Holdout simple (train/test split)
Holdout repetitivo — se repite el split aleatoriamente varias veces y se promedia el error, reduciendo la varianza de la estimación respecto a un holdout único
Validación cruzada (K-Fold, Stratified K-Fold)
Curva de validación para K


### Eficiencia computacional

Complejidad temporal en entrenamiento vs. predicción
Estructuras de datos para búsqueda eficiente: KD-Tree y Ball Tree
KNN aproximado (ANN) para datasets grandes
Librerías optimizadas: scikit-learn, Faiss, Annoy


### Limitaciones y desafíos

Lento en predicción con datasets grandes
Sensibilidad al ruido y outliers
Mal desempeño en alta dimensionalidad
Desbalance de clases
Alto consumo de memoria


### Variantes y extensiones

KNN ponderado
KNN adaptativo (K variable según la densidad local)
KNN para detección de anomalías
KNN como imputador de valores faltantes (KNNImputer en sklearn)


### Implementación práctica

Implementación desde cero en Python
Uso con scikit-learn (KNeighborsClassifier, KNeighborsRegressor)
Pipelines con preprocesamiento + KNN
Grid Search / Random Search para tuning de hiperparámetros


### Casos de uso reales

Sistemas de recomendación
Detección de fraude
Clasificación de imágenes (baseline)
Imputación de datos faltantes
Recuperación de información
