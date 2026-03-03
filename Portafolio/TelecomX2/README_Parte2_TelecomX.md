# 📊 Telecom X -- Parte 2: Modelado Predictivo de Churn

## 🎯 Objetivo del Proyecto

El objetivo de esta segunda fase del proyecto es construir y evaluar
modelos de Machine Learning capaces de predecir la cancelación de
clientes (Churn) en Telecom X.

Mientras que la Parte 1 se enfocó en limpieza y análisis exploratorio,
en esta fase se desarrolla un enfoque predictivo orientado a negocio,
priorizando la detección de clientes con alto riesgo de fuga.

------------------------------------------------------------------------

## 📂 Estructura del Proyecto

telecomx-churn-analysis/ │ ├── telecom_clean.csv\
├── telecomX_parte2.ipynb\
├── README.md

------------------------------------------------------------------------

## 🛠️ Preparación de Datos

En esta fase se realizaron los siguientes pasos:

-   Eliminación de variables irrelevantes (customerID, Cuentas_Diarias)
-   Separación de variables predictoras (X) y variable objetivo (y)
-   División 80/20 (Train/Test) con estratificación
-   One-Hot Encoding para variables categóricas
-   Estandarización con StandardScaler
-   Balanceo de clases mediante SMOTE

### 📊 Distribución de clases

Antes de SMOTE: - Clase 0 (No Churn): 4130 - Clase 1 (Churn): 1495

Después de SMOTE: - Ambas clases balanceadas en 4130 registros

Esto permitió entrenar modelos sin sesgo hacia la clase mayoritaria.

------------------------------------------------------------------------

## 📈 Análisis de Correlación

Variables numéricas clave analizadas:

-   tenure
-   Charges.Monthly
-   Charges.Total

### 🔎 Hallazgos

-   tenure presenta correlación negativa fuerte (-0.35)
-   Charges.Total correlación negativa moderada (-0.19)
-   Charges.Monthly correlación positiva (0.19)

Conclusión: Clientes nuevos con altos cargos mensuales presentan mayor
probabilidad de cancelación.

------------------------------------------------------------------------

## 🤖 Modelos Entrenados

### 1️⃣ Regresión Logística

Accuracy: 0.7484\
Recall (Clase 1): 0.8048\
F1-Score: 0.6297

Detecta el 80.48% de los clientes que cancelan.

------------------------------------------------------------------------

### 2️⃣ Random Forest

Accuracy: 0.7804\
Recall (Clase 1): 0.5856\
F1-Score: 0.5863

Mayor exactitud global pero menor capacidad para detectar churn real.

------------------------------------------------------------------------

## 🏆 Modelo Seleccionado

### ✅ Regresión Logística

Aunque Random Forest tiene mayor Accuracy, la métrica clave en problemas
de Churn es el Recall de la clase 1.

En telecomunicaciones: - Es más costoso perder un cliente (Falso
Negativo) - Que ofrecer una promoción innecesaria (Falso Positivo)

La Regresión Logística captura el 80% de las fugas, por lo tanto es el
modelo más adecuado estratégicamente.

------------------------------------------------------------------------

## 🔎 Interpretación de Variables Relevantes

### 📌 Regresión Logística

Factores de mayor riesgo: - Contract_Month-to-month -
InternetService_Fiber optic - MonthlyCharges altos

Factores de retención: - tenure alto - Contract_Two year

------------------------------------------------------------------------

### 📌 Random Forest

Variables más importantes: - Charges.Total - Charges.Monthly - tenure

Observación: El modelo puede estar sobreajustando variables numéricas.

------------------------------------------------------------------------

## 💡 Recomendaciones Estratégicas

1.  Incentivar contratos a largo plazo.
2.  Crear programas de retención para clientes nuevos.
3.  Revisar planes de alto costo con bajo valor percibido.
4.  Implementar campañas preventivas basadas en score de churn.

------------------------------------------------------------------------

## 🚀 Tecnologías Utilizadas

-   Python
-   Pandas
-   NumPy
-   Scikit-Learn
-   Imbalanced-Learn (SMOTE)
-   Matplotlib
-   Seaborn

------------------------------------------------------------------------

## 📌 Conclusión Final

El proyecto demuestra cómo pasar de análisis descriptivo a decisiones
estratégicas basadas en Machine Learning.

La Regresión Logística se posiciona como el modelo óptimo al priorizar
la detección temprana de clientes en riesgo, alineando el análisis
técnico con el impacto financiero real del negocio.
