Análisis Predictivo de Churn en Telecomunicaciones
Descripción General del Proyecto
Este proyecto tiene como objetivo desarrollar modelos de Machine Learning para predecir la cancelación de clientes (Churn) en una empresa de telecomunicaciones. El análisis se centra en el preprocesamiento de datos, el entrenamiento y evaluación de dos modelos predictivos (Regresión Logística y Random Forest), y la interpretación de la importancia de las variables.

Contenido del Notebook
Extracción de Datos: Carga inicial del conjunto de datos TelecomX_Data.json. Incluye manejo de errores para FileNotFoundError con la creación de un DataFrame de ejemplo.
Preprocesamiento y Limpieza de Datos:
Aplanamiento de Columnas Anidadas: Las columnas con estructuras de diccionario (customer, phone, internet, account) se han expandido en características individuales.
Eliminación de Identificadores: La columna customerID ha sido removida.
Manejo de Valores Nulos y Conversión de Tipos: Se gestionaron valores nulos y se aseguró la correcta tipificación de datos, especialmente en account_Charges.Total.
Limpieza de la Variable Objetivo: Se creó Churn_cleaned para estandarizar la columna de Churn.
Codificación de Variables Categóricas: Aplicación de One-Hot Encoding a todas las características categóricas para convertirlas a un formato numérico.
Balanceo de Clases: Uso de SMOTE (Synthetic Minority Over-sampling Technique) para abordar el desbalanceo de clases en la variable objetivo Churn_cleaned.
Análisis Exploratorio de Datos (EDA):
Visualización de la distribución de Churn_cleaned.
Análisis de la relación entre variables numéricas clave (customer_tenure, account_Charges.Total, account_Charges.Monthly) y Churn_cleaned mediante boxplots.
Separación de Datos: División del conjunto de datos balanceado en conjuntos de entrenamiento (80%) y prueba (20%) para la evaluación del modelo.
Creación y Evaluación de Modelos Predictivos:
Regresión Logística: Modelo entrenado con datos escalados, evaluado con métricas de clasificación y matriz de confusión.
Random Forest: Modelo entrenado con datos sin escalar, evaluado con las mismas métricas.
Análisis de Importancia de Variables:
Extracción y visualización de los coeficientes de la Regresión Logística.
Extracción y visualización de la importancia de las características del Random Forest.
Discusión y comparación de los factores más influyentes según cada modelo.
Resultados Clave y Conclusiones
Rendimiento del Modelo: Ambos modelos lograron un rendimiento perfecto (Accuracy, Precision, Recall, F1-Score de 1.0000) en el conjunto de datos de ejemplo. Se enfatiza que este resultado es irreal para un dataset real y es un artefacto del pequeño tamaño del dummy data.
Impacto de la Normalización: Se confirmó que la Regresión Logística es sensible a la escala de los datos, mientras que Random Forest no lo es, obteniendo resultados perfectos en ambos casos con el dummy data.
Variables Clave en la Predicción de Churn:
customer_tenure (antigüedad del cliente) y account_Charges.Monthly (cargos mensuales) fueron consistentemente identificados como factores críticos por ambos modelos.
El Random Forest destacó la importancia de servicios específicos de internet y sus complementos, lo que sugiere interacciones no lineales.
La Regresión Logística proporcionó una visión lineal de la influencia de las características (dirección y magnitud de los coeficientes).
Uso
Para replicar el análisis:

Asegúrate de tener el archivo TelecomX_Data.json en la ruta /content/ de tu entorno de Colab.
Ejecuta todas las celdas del notebook secuencialmente.
Tecnologías Utilizadas
Python 3.x
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn
Imbalanced-learn (para SMOTE)
