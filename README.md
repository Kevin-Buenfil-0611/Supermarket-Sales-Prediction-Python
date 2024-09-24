# Descripción General
El proyecto "Supermarket Sales" tiene como objetivo predecir patrones de ventas en un supermercado utilizando técnicas de machine learning. El proyecto se estructura en tres notebooks que permiten procesar los datos, entrenar un modelo de predicción y aplicar el modelo en datos nuevos o no vistos previamente.

1. Feature Pipeline Notebook
En esta notebook se realiza la preparación y transformación de los datos de ventas del supermercado. Aquí se incluyen los siguientes pasos:

- Carga de Datos: Se carga el dataset de ventas.
- Preprocesamiento: Se realiza limpieza de los datos, manejo de valores faltantes y transformación de las características. Se incluyen técnicas de codificación de variables categóricas y escalado de características numéricas.
- Exploración de Datos (EDA): Visualización de la distribución de las variables más importantes, análisis de correlación entre variables y revisión de outliers.
- Guardado de Datos: Se almacenan los datos procesados para ser utilizados en las etapas posteriores.


2. Training Pipeline Notebook
En esta segunda notebook, se utiliza un conjunto de datos de entrenamiento para ajustar un modelo de predicción de ventas. Los pasos clave incluyen:

- Carga de Datos Procesados: Se cargan los datos que fueron transformados en la notebook anterior.
- Selección del Modelo: Se prueban varios algoritmos de machine learning (por ejemplo, RandomForest, XGBoost) usando LazyPredict para comparar su rendimiento.
- Entrenamiento del Modelo: Se entrena el mejor modelo seleccionado basado en las métricas de rendimiento (MSE, MAE, etc.).
Registro de Métricas en MLFlow: Las métricas clave como error cuadrático medio (MSE), error absoluto medio (MAE), y exactitud del modelo se registran usando MLFlow.
- Guardado del Modelo: El modelo entrenado se guarda para ser utilizado en el pipeline de inferencia.


3. Batch Inference Pipeline Notebook
En esta notebook, se utiliza el modelo entrenado para realizar predicciones sobre nuevos datos de ventas que no fueron vistos durante el entrenamiento. Las etapas son:

- Carga del Modelo: Se carga el modelo entrenado desde un archivo guardado.
- Predicciones: Se realizan predicciones por lotes sobre nuevos datos, utilizando el modelo cargado.
- Evaluación: Se calculan métricas adicionales si se cuenta con los valores reales para validar la calidad de las predicciones.
- Almacenamiento de Resultados: Las predicciones se almacenan en un archivo de salida que puede ser utilizado para análisis posteriores.

Resultados Esperados

a) Al completar esta etapa, se generan predicciones sobre datos nuevos de ventas del supermercado, las cuales pueden ser utilizadas para la toma de decisiones estratégicas.

Este proyecto permite automatizar el análisis y predicción de las ventas del supermercado, facilitando la optimización de inventarios, promociones y planificación financiera.

Base de datos empleada en el proyecto: [Kaggle Link](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales)