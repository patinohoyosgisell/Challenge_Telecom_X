📊 Challenge Telecom X — Análisis de Evasión de Clientes (Churn)
📌 Descripción del Proyecto

Este proyecto forma parte del Challenge Telecom X de Alura Latam, cuyo objetivo es analizar el comportamiento de los clientes de una empresa de telecomunicaciones para identificar factores asociados a la evasión de clientes (Churn).

La cancelación de clientes representa uno de los principales desafíos para las empresas de telecomunicaciones, ya que impacta directamente en los ingresos y en la sostenibilidad del negocio.

Mediante técnicas de análisis exploratorio de datos (EDA) se busca descubrir patrones que permitan comprender qué características de los clientes están relacionadas con una mayor probabilidad de cancelación.

🎯 Objetivos del Proyecto

Analizar el comportamiento de los clientes de Telecom X.

Identificar factores asociados a la cancelación del servicio.

Explorar relaciones entre variables categóricas y numéricas.

Generar insights estratégicos para mejorar la retención de clientes.

🛠️ Tecnologías Utilizadas

Este proyecto fue desarrollado utilizando:

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab

📂 Estructura del Repositorio
Challenge_Telecom_X
│
├── Challenge_Telecom_XV1.ipynb   # Notebook con el análisis completo
├── Informe_Final.md              # Informe con conclusiones del análisis
├── README.md                     # Descripción del proyecto
└── datos/                        # Dataset utilizado en el análisis
🔎 Análisis Realizado

Durante el análisis se realizaron las siguientes etapas:

1️⃣ Limpieza y Preparación de Datos

Importación del dataset

Estandarización de nombres de columnas

Conversión de variables categóricas (Yes / No → 1 / 0)

Identificación de valores faltantes

Creación de nuevas variables como cuentas_diarias

2️⃣ Análisis Exploratorio de Datos (EDA)

Se analizaron diferentes variables para identificar patrones asociados al churn:

Distribución de cancelación de clientes

Cancelación según género

Cancelación según tipo de contrato

Cancelación según método de pago

Relación entre antigüedad del cliente y cancelación

Análisis de cargos mensuales y cargos totales

Matriz de correlación entre variables numéricas

📊 Principales Insights

El análisis permitió identificar algunos factores importantes asociados a la evasión de clientes:

Los clientes con contratos mensuales presentan mayor probabilidad de cancelar el servicio.

La antigüedad del cliente es uno de los factores más relevantes, ya que los clientes nuevos tienden a cancelar con mayor frecuencia.

Los clientes con cargos mensuales más altos presentan mayor tasa de churn.

El género no muestra una influencia significativa en la cancelación del servicio.

💡 Recomendaciones

A partir de los resultados obtenidos se proponen algunas estrategias para reducir la evasión de clientes:

Incentivar contratos de mayor duración (1 o 2 años).

Implementar programas de fidelización en los primeros meses del cliente.

Analizar la estructura de planes con cargos mensuales más altos.

Diseñar estrategias de retención para clientes con mayor riesgo de cancelación.

🚀 Posibles Mejoras Futuras

Como trabajo futuro se podría:

Implementar modelos de Machine Learning para predicción de churn.

Crear modelos de clasificación (Logistic Regression, Random Forest, XGBoost).

Construir dashboards interactivos para monitoreo de churn.

👩‍💻 Autor

Gisell Patiño Hoyos

Proyecto desarrollado como parte del Challenge Telecom X — Alura Latam.
