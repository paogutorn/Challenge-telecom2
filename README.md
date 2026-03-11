# Análisis Predictivo de Churn en Telecomunicaciones

## 📌 Descripción del Proyecto

Este proyecto desarrolla modelos de **Machine Learning** para predecir la cancelación de clientes (**churn**) en una empresa de telecomunicaciones.

El análisis incluye **limpieza de datos, análisis exploratorio, entrenamiento de modelos y evaluación de resultados** para identificar los factores que influyen en la pérdida de clientes.

Se implementaron dos modelos principales:

* **Regresión Logística**
* **Random Forest**

El objetivo es **identificar clientes con mayor riesgo de cancelación y apoyar estrategias de retención**.

---

# 🔧 Procesamiento de Datos

Las principales etapas de preparación de datos fueron:

* Expansión de columnas anidadas (`customer`, `phone`, `internet`, `account`)
* Eliminación de identificadores como `customerID`
* Manejo de valores nulos y conversión de tipos de datos
* Limpieza de la variable objetivo (`Churn_cleaned`)
* Codificación de variables categóricas mediante **One-Hot Encoding**
* Balanceo de clases utilizando **SMOTE**

---

# 📊 Análisis Exploratorio

Se analizaron variables clave relacionadas con la cancelación de clientes, especialmente:

* `customer_tenure`
* `account_Charges.Monthly`
* `account_Charges.Total`

Las visualizaciones permitieron identificar patrones asociados al **churn**.

---

# 🤖 Modelos de Machine Learning

Se entrenaron y evaluaron dos modelos:

* **Regresión Logística** (requiere datos escalados)
* **Random Forest** (no requiere escalamiento)

Los modelos se evaluaron utilizando:

 Variables Más Importantes

Ambos modelos identificaron como factores clave en la cancelación de clientes:

* **Antigüedad del cliente (`customer_tenure`)**
* **Cargos mensuales (`account_Charges.Monthly`)**

Random Forest también destacó la importancia de **servicios de internet y características adicionales del plan**.

---

# 🛠 Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

✔ Este proyecto demuestra cómo **la ciencia de datos puede ayudar a las empresas a anticipar la pérdida de clientes y tomar decisiones estratégicas basadas en datos.**
