# 📊 TelecomX LATAM – Customer Churn Analysis

Este proyecto analiza la **evasión de clientes (Churn)** en una empresa ficticia de telecomunicaciones en Latinoamérica, utilizando **Python y análisis exploratorio de datos (EDA)** para identificar los factores más relacionados con la cancelación del servicio.

---

## 🎯 Objetivo del Proyecto

Identificar patrones y variables clave que influyen en la evasión de clientes, respondiendo preguntas como:

- ¿Los clientes que pagan más tienden a irse más?
- ¿El tiempo de permanencia (tenure) reduce el churn?
- ¿La cantidad de servicios contratados impacta la probabilidad de evasión?
- ¿Existe relación entre el gasto diario y el churn?

Este análisis sirve como base para futuros **modelos predictivos de churn**.

---

## 🧰 Tecnologías Utilizadas

- Python 🐍
- Pandas
- Matplotlib
- GoogleColab

---

## 📂 Dataset

El dataset (`TelecomX_Data.json`) contiene información de clientes, incluyendo:

- Información demográfica
- Servicios contratados
- Tipo de contrato
- Cargos mensuales y totales
- Estado de churn (Yes / No)

El archivo original tiene una **estructura anidada en JSON**, que fue normalizada usando `pd.json_normalize()`.

---

## 🧹 Limpieza y Preparación de Datos

Principales pasos realizados:

- Normalización del JSON a un DataFrame plano
- Conversión de variables categóricas (`Yes` / `No`) a booleanos
- Conversión de cargos totales a tipo numérico
- Creación de nuevas variables:
  - **Cuenta diaria** (`Monthly / 30`)
  - **Grupos de permanencia (tenure_group)**
  - **Cantidad de servicios contratados**

---

## 📈 Análisis Exploratorio (EDA)

### 🔹 Distribución del Churn
Visualización de la proporción de clientes que permanecen vs los que se van.

<img width="500" height="600" alt="Distribucion_de_Abandono1" src="https://github.com/user-attachments/assets/15cb110b-3bee-4f40-b701-36cc2c6d40a9" />


---

### 🔹 Cargos Mensuales vs Churn
Comparación del gasto mensual entre clientes que se quedan y los que abandonan el servicio.

<img width="500" height="600" alt="cargos_mensuales_vs_churn" src="https://github.com/user-attachments/assets/fb84b1e5-d24a-44e3-aa48-3058767c1e4d" />


**Insight clave:**  
Los clientes con **cargos mensuales más altos muestran una mayor tasa de churn**.

---

### 🔹 Cuenta Diaria vs Churn
Análisis del gasto diario promedio y su relación con la evasión.

<img width="500" height="620" alt="Cargo Diario vs churn" src="https://github.com/user-attachments/assets/a8d9da89-8887-437d-96d5-fa6d2e7258dd" />


Esto permite interpretar el impacto del precio desde una perspectiva más intuitiva para el cliente.

---

### 🔹 Churn por Grupos de Permanencia
Segmentación de clientes según su tiempo en la empresa.

<img width="600" height="300" alt="tiempo_vs_churn" src="https://github.com/user-attachments/assets/0c054aea-caa2-4f5d-9982-0c2537b211cd" />


**Insight clave:**  
Los clientes con menor tenure (0–12 meses) presentan mayor probabilidad de churn.

---

### 🔹 Correlación entre Variables
Matriz de correlación para identificar relaciones lineales entre variables numéricas.



Variables analizadas:
- Churn (binario)
- Cargo mensual
- Cargo diario
- Tenure
- Número de servicios

---

## 📌 Principales Conclusiones

- 📉 **Mayor gasto mensual y diario está asociado a mayor churn**
- ⏳ **Clientes con menor antigüedad son más propensos a irse**
- 📦 **Mayor cantidad de servicios contratados reduce la evasión**
- 📊 La correlación directa con churn es moderada, lo que sugiere que un **modelo multivariable** sería más efectivo

---

## 🚀 Próximos Pasos

- Implementar modelos predictivos:
  - Regresión logística
  - Random Forest
- Feature engineering avanzado
- Evaluación con métricas de clasificación (ROC, F1-score)

---

## 👤 Autor

**Sebastián Ospina**  
Analista de Datos | Ingeniero Industrial | Python | Pandas | EDA

---

📌 *Este proyecto fue desarrollado con fines educativos y de demostración analítica.*
