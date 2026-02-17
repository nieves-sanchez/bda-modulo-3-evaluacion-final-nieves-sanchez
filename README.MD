# Análisis de Customer Loyalty y Flight Activity

## Descripción del proyecto

Este proyecto analiza la actividad de vuelos y la información del programa de fidelización de clientes. Se ha desarrollado como parte de la evaluación final del Módulo 3 del Bootcamp de Data Analytics & IA de Adalab.

El objetivo principal es aplicar un flujo completo de trabajo en análisis de datos, que incluye:

- Preparación y validación de datos.
- Exploración estructurada (EDA).
- Limpieza y transformación.
- Análisis estadístico descriptivo.
- Visualización de resultados.
- Evaluación de posibles diferencias en el comportamiento de reserva de vuelos según el nivel educativo.

Durante todo el proceso se han documentado las decisiones tomadas y se han añadido interpretaciones en lenguaje natural.

---

## Estructura del repositorio

```text
bda-modulo-3-evaluacion-final-nieves-sanchez/
│
├── data/
│ ├── raw/
│ │ ├── Customer Flight Activity.csv
│ │ └── Customer Loyalty History.csv
│ │
│ └── processed/
│ ├── dataset_unido.csv
│ └── cleaned_customer_loyalty_flights.csv
│
├── notebooks/
│ ├── 01_preparacion_y_merge.ipynb
│ ├── 02_EDA.ipynb
│ ├── 03_limpieza.ipynb
│ └── 04_analisis.ipynb
│
└── README.md
```

---

## Flujo de trabajo

### 1. Preparación y unión de datos

Notebook: `01_preparacion_y_merge.ipynb`

- Validación de claves.
- Detección y eliminación de duplicados exactos.
- Consolidación a nivel cliente–año–mes.
- Unión de los datasets de actividad y fidelización.
- Exportación del dataset unido.

---

### 2. Análisis exploratorio (EDA)

Notebook: `02_EDA.ipynb`

- Revisión de estructura del dataset y tipos de datos.
- Análisis de valores nulos (conteo y porcentaje).
- Exploración de la variable `salary` (resumen estadístico, valores negativos y distribución).
- Detección preliminar de valores atípicos en variables numéricas mediante el método IQR.
- Revisión de variables categóricas (frecuencias y coherencia de categorías).
- Validaciones de coherencia en variables numéricas (rangos, valores negativos e inconsistencias).

---

### 3. Limpieza de datos

Notebook: `03_limpieza.ipynb`

Decisiones tomadas tras el EDA:

- Normalización de nombres de columnas (snake_case).
- Creación de la variable booleana `cancelled`.
- Tratamiento de `salary`:
  - Corrección de valores negativos.
  - Imputación mediante la mediana por nivel educativo.
- Eliminación de variables constantes.
- Aplicación de `strip()` en variables categóricas.
- Exportación del dataset limpio final.

Dataset final:
`cleaned_customer_loyalty_flights.csv`

---

### 4. Análisis estadístico y visualización

Notebook: `04_analisis.ipynb`

Incluye:

- Estadísticas descriptivas (media, mediana, desviación estándar).
- Detección de valores atípicos (IQR) con apoyo visual (boxplots).
- Análisis de correlación entre variables numéricas mediante Spearman (más robusto ante outliers).
- Distribución de variables categóricas.
- Visualizaciones para responder a las preguntas del enunciado:
  - Vuelos reservados por mes.
  - Relación entre distancia y puntos acumulados.
  - Distribución de clientes por provincia.
  - Salario promedio por nivel educativo.
  - Proporción por tipo de tarjeta.
  - Distribución por estado civil y género.
- Evaluación descriptiva de `flights_booked` según `education`.

---

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Atribución académica

Este proyecto ha sido desarrollado por:

Nieves Sánchez

Como parte de la evaluación final del Módulo 3 del Bootcamp de Data Analytics & IA de Adalab.

Repositorio con fines académicos y de portfolio profesional.

## Contacto

- [LinkedIn](https://www.linkedin.com/in/nieves-sanchez-data)
- [GitHub](https://github.com/nieves-sanchez)
