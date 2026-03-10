# 📊 Informe Final — Análisis de Evasión de Clientes (Churn)

## Introducción

La evasión de clientes, también conocida como **Churn**, representa uno de los principales desafíos para las empresas de telecomunicaciones. La cancelación de servicios por parte de los clientes puede generar pérdidas significativas de ingresos y afectar la estabilidad del negocio.

El objetivo de este proyecto es **analizar los datos de clientes de Telecom X para identificar patrones asociados a la cancelación del servicio**. A través de técnicas de **análisis exploratorio de datos (EDA)**, se busca comprender qué características o comportamientos de los clientes están relacionados con una mayor probabilidad de evasión.

Este análisis permitirá generar **insights estratégicos** que puedan ayudar a la empresa a diseñar acciones orientadas a mejorar la retención de clientes y reducir el churn.

---

# Limpieza y Tratamiento de Datos

Para preparar el dataset para el análisis, se realizaron diversas etapas de limpieza y transformación de los datos.

## Importación de datos

Los datos fueron importados desde el repositorio del challenge y cargados en un **DataFrame utilizando la librería Pandas**.

## Estandarización de nombres de columnas

Se renombraron las columnas al español con el objetivo de facilitar la interpretación del dataset.

| Nombre original | Nuevo nombre |
|---|---|
| customerID | id_cliente |
| Churn | cancelacion |
| customer.tenure | cliente.antiguedad |
| account.charges.monthly | cuenta.cargos_mensuales |
| account.charges.total | cuenta.cargos_totales |

## Tratamiento de valores categóricos

Las variables con valores **Yes / No** fueron convertidas a valores binarios:

- Yes → 1  
- No → 0  

Esto facilita el análisis estadístico y permite calcular correlaciones entre variables.

## Identificación de valores faltantes

Durante el proceso se detectaron **224 valores vacíos en la variable cancelacion**, los cuales fueron analizados para mantener la consistencia del dataset.

## Creación de nuevas variables

Se creó la variable **cuentas_diarias**, calculada a partir de los cargos mensuales:

cuentas_diarias = cuenta.cargos_mensuales / 30

Esta variable permite analizar el gasto de los clientes con mayor nivel de detalle.

---

# Análisis Exploratorio de Datos

Se realizó un análisis exploratorio para identificar patrones y relaciones entre las variables y la cancelación de clientes.

## Distribución de Cancelación de Clientes

Se analizó la proporción de clientes que cancelaron el servicio frente a los que permanecen activos.

Los resultados muestran que **la mayoría de los clientes permanece activa**, sin embargo existe un porcentaje importante que cancela el servicio, lo cual representa una oportunidad de mejora para la empresa.

---

# Cancelación según variables categóricas

Se analizaron diferentes variables categóricas para identificar perfiles de clientes con mayor tendencia a cancelar.

## Género

El análisis muestra que **no existe una diferencia significativa en la tasa de cancelación entre hombres y mujeres**, lo que indica que el género no es un factor determinante en el churn.

## Tipo de contrato

El tipo de contrato presenta uno de los patrones más claros:

- Los clientes con contrato **Month-to-month (mensual)** presentan la mayor tasa de cancelación.
- Los contratos de **uno o dos años** muestran una mayor retención de clientes.

Esto sugiere que **los contratos de mayor duración contribuyen a reducir la evasión**.

## Método de pago

Se observó que algunos métodos de pago presentan **mayor tasa de cancelación**, lo que podría estar asociado a perfiles específicos de clientes o a menor compromiso con el servicio.

---

# Análisis de variables numéricas

También se analizaron variables numéricas para identificar diferencias entre clientes activos y clientes que cancelaron.

## Antigüedad del cliente

El análisis muestra que los clientes que cancelan el servicio suelen tener **menor antigüedad**, lo que indica que el riesgo de evasión es mayor durante los primeros meses de relación con la empresa.

## Cargos mensuales

Se observa que los clientes que cancelan tienden a tener **cargos mensuales ligeramente más altos**, lo que podría indicar sensibilidad al precio.

## Cargos totales

Los clientes que permanecen activos tienen **mayores cargos totales acumulados**, lo cual es consistente con una mayor permanencia en la empresa.

---

# Conclusiones e Insights

A partir del análisis exploratorio se identificaron varios factores asociados con la evasión de clientes.

Los principales hallazgos son:

- Los clientes con **contratos mensuales presentan la mayor tasa de cancelación**.
- La **antigüedad del cliente es uno de los factores más importantes**, ya que los clientes nuevos cancelan con mayor frecuencia.
- Los clientes con **cargos mensuales más altos tienden a mostrar mayor probabilidad de churn**.
- El **género no parece tener impacto significativo** en la cancelación del servicio.

Estos resultados permiten comprender mejor el comportamiento de los clientes y detectar **segmentos con mayor riesgo de abandono**.

---

# Recomendaciones Estratégicas

Con base en los hallazgos del análisis, se proponen las siguientes estrategias para reducir la evasión de clientes.

## Incentivar contratos de largo plazo

Promover contratos de **uno o dos años** mediante descuentos o beneficios adicionales para aumentar la retención.

## Fortalecer la experiencia del cliente en los primeros meses

Dado que la mayor evasión ocurre en los primeros meses, se recomienda implementar **programas de onboarding y acompañamiento al cliente** durante esta etapa.

## Revisar la estructura de precios

Analizar los planes con **cargos mensuales más altos**, evaluando si ofrecen suficiente valor percibido para los clientes.

## Programas de fidelización

Implementar **programas de beneficios o recompensas para clientes con mayor antigüedad**, incentivando su permanencia.
