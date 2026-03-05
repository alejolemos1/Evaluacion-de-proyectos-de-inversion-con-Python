# Evaluación de proyectos de inversión con Python

## Objetivos
La idea de este proyecto es crear un modelo que obtenga datos de un excel sobre los free cash flows de distintos proyectos de inversion, los evalúe y los compare de forma automatica, simulando el proceso que haría con excel un analísta pero para lotes de proyectos, cuyo analisis se volvería exageradamente largo y tedioso.

## Proyecto
### Recursos necesarios
Lo primero que hice fue instalar e importar los recursos necesarios: pandas, numpy, numpy-financial y matplotlib.
Al usar google colab, solo fue necesario instalar numpy financial.
### Carga de datos
Los flujos de los proyectos se encuentran en un archivo de excel, cada fila es un proyecto, con la primera columna como nombre o identificador, seguido de una columna para cada año.
Al importarlo con Pandas, se ve algo así:

<img width="487" height="320" alt="image" src="https://github.com/user-attachments/assets/6c76d908-bfee-4989-9042-a0ae0eb213f3" />

### Calculo de indicadores
Utilizando en conjunto Pandas, Numpy y Numpy Financial, calculamos VAN, TIR, TIRM, Payback y Discounted Payback, se genera el siguiente DataFrame como resumen ordenado por VAN:

<img width="671" height="323" alt="image" src="https://github.com/user-attachments/assets/54d835cf-dfa5-48d1-9bd0-bd6d07d635ac" />

Se asume un WACC constante del 10% únicamente con fines ilustrativos para calcular VAN, TIR y MIRR.

### Comparación visual

Por último, utilizando Matplotlib, se genera un grafico de barras mostrando en comparacion el VAN de cada proyecto, con colores que permiten identificar rápidamente los proyectos que generan valor y los que lo destruyen, asi como el orden de mayor a menor VAN.

<img width="600" height="432" alt="image" src="https://github.com/user-attachments/assets/e9924470-c937-4023-9454-5f316fdbf168" />

## Próximos pasos
1. Optimizar código
2. Añadir análisis de sensibilidad a la tasa de descuento
3. Exportar automáticamente resultados en un archivo excel
4. Comparar con Valor Anual Equivalente para proyectos de distinta duración
