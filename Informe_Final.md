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
