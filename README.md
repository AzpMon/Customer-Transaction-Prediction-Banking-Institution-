# Predicción de Transacciones de Clientes en Instituciones Bancarias

Alejandro Monroy Azpeitia, 7 de agosto de 2024

## Descripción del Proyecto
Este proyecto tiene como objetivo predecir qué clientes realizarán una transacción específica en el futuro, independientemente de la cantidad de dinero transaccionado. El conjunto de datos utilizado en este proyecto proviene de Kaggle y es proporcionado por Santander. El proyecto involucra un análisis exploratorio de datos (EDA) extenso utilizando PySpark con consultas similares a SQL para manipular y explorar los datos de manera eficiente. Un desafío significativo abordado en este proyecto es el problema de clasificación binaria con datos potencialmente desequilibrados.

## Descripción del Conjunto de Datos
El conjunto de datos incluye varios archivos CSV con información sobre transacciones de clientes. Aquí se presentan los archivos principales utilizados:

## Análisis Exploratorio de Datos (usando  PySpark y consultas tipo SQL)
En la fase de EDA, se realizó un análisis de datos extenso utilizando PySpark, aprovechando las consultas similares a SQL para la manipulación y exploración eficiente de datos. Se emplearon las siguientes estrategias:

1. **Lectura y Carga de Datos**: El archivo CSV fue leído y cargado en un DataFrame de PySpark.
2. **Consultas Similares a SQL**: Se utilizaron las capacidades SQL de PySpark para realizar transformaciones de datos y calcular estadísticas.
3. **Desequilibrio de Datos**: Se abordó el desafío de los datos desequilibrados, donde el número de ejemplos positivos y negativos en la variable objetivo difiere significativamente.
4. **Corrección de Tipos de Datos**: Se corrigieron los tipos de datos de cada columna para garantizar la consistencia y precisión.
5. **Análisis de Valores Atípicos**: Se identificaron valores atípicos utilizando métodos estadísticos y visualizaciones.
6. **Manejo de Valores Nulos**: Se analizaron posibles valores nulos.
7. **Análisis de Correlación**: Se utilizaron matrices de correlación para identificar relaciones entre variables.

## Entrenamiento de Modelos
Se utilizó un cuaderno de Jupyter separado para entrenar diferentes modelos. En todos ellos, se realizó un análisis PCA para reducir el número de columnas de 200 a 79, con un porcentaje de varianza explicada mayor al 0.8.

### XGBoost con Optimización de Hiperparámetros (usando XGBoost y Optuna)
- Se utilizó Optuna para la optimización de hiperparámetros con validación cruzada.
- Se evaluó utilizando curvas AUC-ROC para los datos de entrenamiento y prueba.
- Se trazaron curvas ROC y se visualizaron recall, precisión y F1-Score contra diferentes umbrales de probabilidad.
- Se seleccionó el mejor modelo y se mostró la matriz de confusión.

### Regresión Logística con Balanceo de Datos (usando MLlib de PySpark)
- **Submuestreo**: Se utilizó para abordar el desequilibrio de datos reduciendo las instancias de la clase mayoritaria.
- **Búsqueda en Rejilla para Hiperparámetros**: Se realizó mediante búsqueda en rejilla para encontrar los mejores parámetros.
- **Evaluación**: Se evaluaron los modelos utilizando curvas ROC, recall, precisión y F1-Score.
- Se seleccionó el mejor modelo y se mostró la matriz de confusión.

### Contacto
Para cualquier pregunta o retroalimentación, contáctame en:

amonroy.azpeitia@gmail.com

[https://www.linkedin.com/in/alejandromonroyazpeitia/](https://www.linkedin.com/in/alejandromonroyazpeitia/)
