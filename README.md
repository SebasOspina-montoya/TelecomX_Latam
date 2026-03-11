# 📊 TelecomX - Análisis de Cancelación de Clientes (Churn)

## 📌 Descripción del proyecto

TelecomX es una empresa de telecomunicaciones que actualmente enfrenta un problema relacionado con la cancelación de sus servicios por parte de los clientes.

El objetivo de este proyecto es analizar los datos disponibles para identificar posibles factores que estén influyendo en el abandono del servicio (Churn) y generar insights que permitan tomar decisiones estratégicas para reducir la pérdida de clientes.

El análisis se realizó utilizando Python en un notebook de Google Colab, aplicando técnicas de limpieza de datos, transformación y análisis exploratorio.

---

# 🗂 Estructura del proyecto

El proyecto se compone de los siguientes archivos:

- TelecomX_LATAM.ipynb → Notebook con todo el análisis del proyecto
- TelecomX_Data.json → Base de datos utilizada para el análisis
- Gráficos generados → Visualizaciones utilizadas para el análisis exploratorio

---

# 🛠 Tecnologías utilizadas

Las principales herramientas utilizadas fueron:

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab

---

# 📥 Extracción de datos

Primero se cargó la base de datos en formato JSON dentro del notebook utilizando la librería Pandas.

Se utilizó la función `pd.read_json()` para cargar la información.

Debido a que los datos contenían estructuras anidadas dentro de diccionarios, fue necesario normalizar la base de datos utilizando `pd.json_normalize()` para transformar los datos en un formato tabular que permitiera su análisis.

---

# 🔧 Limpieza y transformación de datos

Durante esta etapa se realizaron varias tareas importantes:

- Revisión de la estructura de la base de datos
- Identificación de valores nulos
- Cambio de nombres de columnas para facilitar su manipulación
- Eliminación de registros con valores vacíos en columnas importantes
- Conversión de variables categóricas
- Creación de nuevas variables para el análisis

Primero se revisó la información general del dataset utilizando `df.info()` para conocer los tipos de datos y detectar valores nulos.

Posteriormente se renombraron varias columnas para facilitar su manejo dentro del análisis.

Durante la revisión se detectaron valores vacíos en las columnas **Churn** y **Total**, por lo que se eliminaron estos registros para evitar problemas en el análisis.

Luego se creó una nueva variable llamada **Cuentas_Diarias**, que representa el costo diario del servicio de cada cliente.

Esta variable se calculó dividiendo el cargo mensual entre 30 días.

También se convirtieron varias variables categóricas que contenían valores **Yes / No** en valores booleanos para facilitar su análisis.

---

# 📊 Análisis exploratorio de datos (EDA)

En esta etapa se realizaron diferentes análisis para identificar patrones relacionados con el churn.

Primero se obtuvieron estadísticas descriptivas utilizando `df.describe()`.

Posteriormente se generó un gráfico de distribución del churn que permitió identificar qué proporción de clientes cancela el servicio.

El análisis mostró que aproximadamente **26.6% de los clientes han cancelado el servicio**, mientras que el resto continúa activo.

Luego se realizaron diferentes agrupaciones utilizando `groupby` para analizar la relación entre el churn y distintas variables como:

- Partner
- SeniorCitizen
- Gender
- Dependents
- InternetService
- Contract
- PaymentMethod

También se realizaron varias visualizaciones para entender mejor el comportamiento de los datos.

Entre los gráficos generados se encuentran:

- Distribución de churn
- Boxplot de cargos mensuales vs churn
- Cargos mensuales vs tiempo de permanencia
- Tiempo de permanencia vs churn

Estos análisis permitieron identificar patrones importantes relacionados con el abandono del servicio.

---

# 🔎 Principales hallazgos

A partir del análisis se identificaron varios factores relacionados con la cancelación del servicio.

Los clientes con **cargos mensuales más altos** presentan mayor probabilidad de cancelar el servicio.

También se observó que los clientes con **mayor tiempo en la empresa** tienen menor probabilidad de abandonar el servicio, lo que indica que la fidelización es un factor importante para la retención.

Otro hallazgo importante es que los clientes con **mayor número de servicios contratados** tienen menor probabilidad de cancelar, lo que sugiere que la integración del cliente con múltiples servicios reduce el churn.

---

# 💡 Recomendaciones

A partir de los resultados obtenidos se pueden plantear varias estrategias para reducir el churn:

- Implementar estrategias de fidelización durante los primeros meses del cliente.
- Analizar la estructura de precios para evitar que cargos elevados generen cancelaciones.
- Incentivar la contratación de múltiples servicios dentro de la empresa.
- Desarrollar programas de retención enfocados en clientes con alto riesgo de abandono.

---

# 📈 Conclusión

El análisis exploratorio permitió identificar varios factores que influyen en la cancelación del servicio.

Los resultados obtenidos pueden servir como base para futuros análisis más avanzados, como el desarrollo de modelos predictivos que permitan anticipar qué clientes tienen mayor probabilidad de abandonar el servicio y así implementar estrategias de retención más efectivas.
df = pd.read_json('TelecomX_Data.json')


**Sebastián Ospina**  
Analista de Datos | Ingeniero Industrial | Python | Pandas | EDA

---

📌 *Este proyecto fue desarrollado con fines educativos y de demostración analítica.*
