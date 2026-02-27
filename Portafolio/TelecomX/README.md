# 📊 Telecom X - Análisis de Evasión de Clientes (Churn)

## 🎯 Propósito del Proyecto

El objetivo de este proyecto es analizar el fenómeno de **evasión de
clientes (Churn)** en la empresa Telecom X.\
La cancelación de clientes representa un desafío estratégico clave, ya
que retener clientes existentes es significativamente más rentable que
adquirir nuevos.

Este análisis busca:

-   Identificar patrones asociados a la cancelación.
-   Detectar variables que influyen en la evasión.
-   Generar insights estratégicos basados en datos.
-   Proponer recomendaciones accionables para reducir el churn.

------------------------------------------------------------------------

## 🗂 Estructura del Proyecto

    TelecomX/
    │
    ├── TelecomX.ipynb        # Notebook principal con todo el análisis
    ├── README.md             # Documentación del proyecto
    └── dataset               # Fuente de datos (archivo JSON original)

### 🔎 Organización del Notebook

1.  Importación y carga de datos
2.  Limpieza y tratamiento de datos
3.  Transformación de variables
4.  Análisis exploratorio (EDA)
5.  Visualizaciones
6.  Análisis estratégico
7.  Conclusiones y recomendaciones

------------------------------------------------------------------------

## 📈 Ejemplos de Análisis y Gráficos

Durante el análisis exploratorio se realizaron:

### 📊 Distribución de Churn

-   Comparación entre clientes que cancelan vs. permanecen.
-   Identificación de proporción de evasión.

### 📄 Tipo de Contrato vs Churn

-   Clientes con contrato mensual presentan mayor tasa de cancelación.
-   Contratos anuales muestran menor evasión.

### 💰 Variables Numéricas

Se analizaron:

-   `tenure` (antigüedad del cliente)
-   `Charges.Monthly` (cargo mensual)
-   `Charges.Total` (gasto total acumulado)

#### Insights Clave:

-   Los clientes que cancelan tienen menor tiempo de permanencia.
-   Los cargos mensuales más altos se asocian con mayor churn.
-   La evasión ocurre principalmente en los primeros meses del ciclo de
    vida.

------------------------------------------------------------------------

## 🧠 Principales Insights

1.  📉 La evasión ocurre temprano en la relación con el cliente.
2.  💳 Los clientes con cargos mensuales más altos cancelan más.
3.  📄 Los contratos de largo plazo reducen significativamente el churn.
4.  💰 Clientes con mayor gasto acumulado tienden a permanecer.

------------------------------------------------------------------------

## 🚀 Recomendaciones Estratégicas

-   Implementar programas de retención temprana.
-   Incentivar contratos de largo plazo.
-   Analizar estructura de precios en segmentos de alto churn.
-   Desarrollar un modelo predictivo de churn como siguiente etapa.

------------------------------------------------------------------------

## ⚙️ Instrucciones para Ejecutar el Proyecto

### 1️⃣ Clonar el repositorio

    git clone <URL-del-repositorio>
    cd TelecomX

### 2️⃣ Instalar dependencias

Se recomienda usar un entorno virtual.

    pip install pandas matplotlib requests

### 3️⃣ Ejecutar el Notebook

Abrir:

    TelecomX.ipynb

En:

-   Google Colab
-   Jupyter Notebook
-   VS Code

Ejecutar las celdas en orden para reproducir el análisis completo.

------------------------------------------------------------------------

## 🏁 Conclusión

Este proyecto demuestra cómo transformar datos en decisiones
estratégicas mediante análisis exploratorio y visualización.\
La identificación temprana de patrones de evasión permite diseñar
acciones que aumenten la retención y mejoren la rentabilidad del
negocio.

------------------------------------------------------------------------

📌 Proyecto desarrollado como parte del desafío de análisis de datos -
Telecom X.
