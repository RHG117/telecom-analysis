# 📊 ConnectaTel – Análisis de Segmentación y Uso de Clientes
## Cómo funciona...

Descargar los tres csv files

1. plans.csv
2. usage.csv
3. users_latam.csv

Y cargalos en el tu notebook.

El proyecto funciona con google colab.

Las librerias que use:

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt 

import numpy as np

## 📌 Descripción del Proyecto

Este proyecto analiza el comportamiento de los clientes de ConnectaTel, enfocándose en:

Limpieza y validación de datos

Análisis exploratorio (EDA)

Detección de outliers

Segmentación por edad y nivel de uso

Generación de insights ejecutivos para el negocio

El objetivo es identificar patrones de consumo y oportunidades estratégicas para optimizar la oferta de planes.

##⚠️ Problemas Detectados en los Datos

Durante la fase de exploración se identificaron y corrigieron los siguientes problemas:

🔹 1. Valores Sentinela y Datos Faltantes

En age, se reemplazó el valor sentinela -999 por la mediana.

En city, se reemplazó el sentinela "?" por pd.NA.

La variable city presentaba un 11.7% de valores nulos.

Existencia de valores nulos en variables de uso (mensajes, llamadas y minutos), asociados a registros sin actividad.

🔹 2. Fechas Fuera de Rango

Se convirtieron reg_date y date a tipo fecha.

Se marcaron como nulas (pd.NA) fechas fuera de rango (ej. fechas del 2026).

🔹 3. Distribución y Valores Extremos

Variables de consumo presentan sesgo a la derecha.

Se identificaron outliers en minutos de llamada (usuarios con más de 60 minutos acumulados).

##📌 En general, los datos fueron utilizables tras una limpieza básica y validación de coherencia.

🔍 Segmentación por Edad

Se definieron tres segmentos:

Joven: menor a 30 años

Adulto: entre 30 y 60 años

Adulto mayor: mayor a 60 años

##📊 Hallazgos

El segmento Adulto concentra la mayor cantidad de clientes (más de 1200 usuarios en plan Básico).

Le sigue el segmento Adulto mayor.

El grupo Joven representa la menor proporción.

📌 La edad no mostró ser un factor determinante en la elección del plan.

📊 Segmentación por Nivel de Uso

Se clasificó a los usuarios según su actividad en llamadas y mensajes:

Bajo uso: llamadas < 5 y mensajes < 5

Uso medio: llamadas < 10 y mensajes < 10

Alto uso: resto de los casos

📈 Hallazgos

La mayoría de los usuarios pertenece al grupo Uso medio (más de 1750 usuarios en el plan Básico).

El grupo Alto uso es minoritario, pero estratégicamente relevante.

Las variables de uso presentan sesgo a la derecha, especialmente en minutos de llamada.

Usuarios con más de 60 minutos representan consumo extremo.

📌 El consumo no está distribuido uniformemente: un grupo reducido concentra gran parte del uso.

🚨 Patrones de Uso Extremo (Outliers)

Se detectaron valores extremos principalmente en:

Minutos totales de llamada

Implicaciones:

No parecen errores de captura.

Representan usuarios intensivos.

Pueden ser altamente rentables.

Generan oportunidad para diseño de planes especializados.

💡 Recomendaciones Estratégicas
1️⃣ Diseñar un plan para Alto Uso

Mayor capacidad de minutos.

Beneficios diferenciados.

Estrategia de upselling desde Uso medio.

2️⃣ Optimizar el Plan Básico

Mayoría de clientes está en Uso medio.

Ajustar beneficios para evitar fuga hacia competidores.

3️⃣ Segmentación basada en comportamiento

La edad no es variable diferenciadora.

El nivel de uso es mejor criterio para personalización.

4️⃣ Estrategia Comercial Recomendada

Bajo uso → planes económicos con beneficios digitales.

Uso medio → plan estándar optimizado.

Alto uso → plan premium o ilimitado.

🎯 Conclusión

El principal hallazgo del análisis es que:

El comportamiento de uso explica mejor las diferencias entre clientes que las variables demográficas.

Por lo tanto, ConnectaTel debería enfocar su estrategia en segmentación conductual para:

Mejorar rentabilidad

Diseñar planes más competitivos

Optimizar retención y upselling

Maximizar valor por cliente

##🛠️ Tecnologías Utilizadas

Python

Pandas

NumPy

Seaborn

Matplotlib
