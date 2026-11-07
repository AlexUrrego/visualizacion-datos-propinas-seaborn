# Visualización de datos con Matplotlib y Seaborn

Notebook de **Python** que explora el dataset de propinas de un restaurante (`tips`, incluido en Seaborn) y construye cuatro visualizaciones aplicando principios de diseño visual y percepción humana.

## Qué muestra este proyecto

- Exploración inicial: tipos de datos, nulos, estadísticos descriptivos y frecuencias.
- Variable derivada: porcentaje de propina respecto a la cuenta.
- Configuración global de estilo con una **paleta accesible para daltonismo** (`colorblind`).
- Justificación de cada tipo de gráfico según el tipo de dato.

## Visualizaciones

| Gráfico                | Tipo de dato                             | Pregunta que responde                                     |
| ---------------------- | ---------------------------------------- | --------------------------------------------------------- |
| Barras                 | Categórico frente a numérico             | ¿Qué día tiene la cuenta promedio más alta?               |
| Dispersión             | Dos variables numéricas y una categórica | ¿Cómo se relacionan la cuenta y la propina?               |
| Líneas con media móvil | Serie temporal                           | ¿Cómo evolucionan los ingresos por semana?                |
| Boxplot                | Numérica segmentada por dos categóricas  | ¿Cambia el porcentaje de propina según el día y el turno? |

## Hallazgos principales

- El **domingo** tiene la cuenta promedio más alta (≈ 21.4 USD), seguido del sábado (≈ 20.4 USD).
- Existe una correlación positiva entre cuenta y propina (r ≈ 0.68).
- El porcentaje de propina es bastante estable (mediana ≈ 15.5 %) entre días y turnos.

## Cómo ejecutarlo

**Requisito:** Python 3.

```
pip install -r requirements.txt
jupyter notebook visualizacion_datos_propinas.ipynb
```

El dataset se descarga automáticamente con `sns.load_dataset("tips")`, por lo que la primera ejecución necesita conexión a internet.

## Notas

- El dataset original **no tiene fechas**. Para practicar la visualización temporal se **simuló una columna `date`** (26 semanas de 2023, con el día de la semana coherente con la columna `day`). Por eso ese gráfico no permite sacar conclusiones reales de estacionalidad.
- Datos: dataset `tips` de Seaborn, de uso público para práctica.
