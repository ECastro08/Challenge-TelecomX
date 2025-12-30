# 📊 Telecom X – Análisis de Evasión de Clientes (Churn)

**Autor:** Eduardo Castro  
**Challenge:** Alura Challenge – Data Analytics  
**Proyecto:** Telecom X – Churn de Clientes  

---

## 🧠 Introducción

Telecom X enfrenta una alta tasa de evasión de clientes (*churn*), lo que representa un reto estratégico para la sostenibilidad del negocio.  
Este proyecto tiene como objetivo **analizar los datos de clientes** para identificar patrones y factores asociados a la cancelación del servicio, apoyando al equipo de Data Science en la creación de **modelos predictivos y estrategias de retención**.

El análisis se realizó utilizando **Python** y las principales bibliotecas de análisis y visualización de datos.

---

## 🎯 Objetivos del Proyecto

- Comprender la distribución de la evasión de clientes.
- Identificar variables categóricas y numéricas relacionadas con el churn.
- Analizar correlaciones entre variables clave.
- Generar insights accionables para reducir la tasa de cancelación.
- Sentar bases para futuros modelos de Machine Learning.

---

## 🧹 Limpieza y Tratamiento de Datos

Durante el preprocesamiento de los datos se realizaron las siguientes acciones:

- Eliminación de registros inconsistentes en la variable `churn`.
- Conversión de variables numéricas (`total_charges`, `monthly_charges`) a su tipo correcto.
- Estandarización de variables binarias (`Yes / No` → `1 / 0`).
- Renombrado de columnas para mejorar legibilidad y consistencia.
- Creación de nuevas variables derivadas, como:
  - `cuentas_diarias`
  - `num_servicios` (cantidad de servicios contratados)

Dataset final: **7043 registros sin valores nulos**.

---

## 📊 Análisis Exploratorio de Datos (EDA)

### 🔹 Distribución de Churn
- Se analizó la proporción de clientes que cancelaron vs. los que permanecen activos.
- Se confirmó que la evasión representa un problema significativo para la empresa.

### 🔹 Variables Categóricas
Se exploró la evasión según:
- Género
- Tipo de contrato
- Método de pago

Se identificaron mayores tasas de churn en:
- Contratos de corto plazo
- Métodos de pago electrónicos
- Clientes con facturación sin papel

### 🔹 Variables Numéricas
Se analizó la relación entre churn y:
- Tiempo de permanencia (`tenure`)
- Cargos mensuales
- Total gastado
- Cuenta diaria

Clientes con **menor antigüedad** y **cargos más altos** presentan mayor tendencia a cancelar.

---

## 🔗 Análisis de Correlación

Se realizó un análisis de correlación entre variables numéricas utilizando `corr()` de Pandas y mapas de calor.

**Principales hallazgos:**
- `tenure` y `num_servicios` tienen correlación negativa con el churn.
- `monthly_charges` y `cuentas_diarias` muestran relación positiva con la evasión.
- Los clientes con más servicios contratados tienden a permanecer más tiempo.

Este análisis es clave para el desarrollo de **modelos predictivos más robustos**.

---

## 📌 Conclusiones e Insights

- La evasión está fuertemente asociada a clientes nuevos.
- Contratos mensuales presentan mayor churn que contratos anuales.
- Clientes con menos servicios contratados son más propensos a cancelar.
- Costos elevados influyen significativamente en la decisión de evasión.

---

## 💡 Recomendaciones

- Incentivar contratos de largo plazo con beneficios exclusivos.
- Diseñar paquetes de servicios para aumentar la fidelización.
- Implementar estrategias de retención temprana para nuevos clientes.
- Revisar la estructura de costos para clientes con cargos elevados.

---

## 🚀 Próximos Pasos

- Implementación de modelos predictivos (Regresión Logística, Árboles de Decisión).
- Evaluación de métricas (Precision, Recall, ROC-AUC).
- Segmentación de clientes para campañas de retención.

---

## 🛠️ Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

📘 *Este proyecto forma parte del programa de formación de Alura y representa un ejercicio práctico de análisis de datos aplicado a un caso real de negocio.*
