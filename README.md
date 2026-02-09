# Movilidad-Urbana-y-Productividad-Econ-mica-en-LATAM

Análisis integral que combina datos de movilidad urbana (TomTom Traffic Index) y datos económicos urbanos (OECD Cities) para evaluar cómo la congestión, los tiempos de viaje y el tráfico se relacionan con la productividad económica en ciudades latinoamericanas.

Tecnologías: Python, pandas, numpy, seaborn, matplotlib, Jupyter Notebook, limpieza y unión de datasets, análisis exploratorio de datos (EDA), validación de tipos, agregación por ciudad–año, visualización de relaciones entre variables.

## 1. Contexto del Proyecto

Este proyecto analiza la relación entre la movilidad urbana —medida a través de congestión, tiempos de viaje y retrasos— y la productividad económica —representada por el PIB per cápita— en 14 ciudades de 7 países de Latinoamérica durante el año 2024. El objetivo fue determinar si existe una correlación entre el nivel de tráfico y el desempeño económico de cada ciudad, y qué factores podrían explicar diferencias significativas entre mercados. Para ello, trabajé con dos datasets independientes (tráfico y economía), que integré mediante limpieza, estandarización y unión por ciudad y año. El análisis buscó identificar patrones, anomalías y oportunidades de mejora para la planificación urbana y la toma de decisiones públicas.

## 2. Análisis Realizado

El proceso inició con la importación de librerías (pandas, numpy, seaborn, matplotlib), exploración de estructura y tipos de datos, y limpieza general: conversión de fechas a formato datetime, corrección de valores numéricos y estandarización de nombres de columnas a snake_case. Posteriormente filtré el año 2024 y agregué métricas de tráfico por ciudad–año, calculando promedios de congestión y tiempos de viaje.
Luego integré ambos datasets mediante una unión INNER usando city y year como claves, asegurando que solo se analizaran ciudades presentes en ambas fuentes. Para validar la calidad de los datos, generé boxplots para detectar outliers, histogramas para revisar distribuciones del PIB per cápita y gráficos comparativos para evaluar tendencias entre tráfico y productividad.

<img width="328" height="272" alt="image" src="https://github.com/user-attachments/assets/8501a549-1bd6-4d7f-8ec1-ed12271cd7c7" />

<img width="425" height="238" alt="image" src="https://github.com/user-attachments/assets/8f42a6fc-0a10-4c9f-b8b9-fc72807f059b" />

<img width="311" height="230" alt="image" src="https://github.com/user-attachments/assets/e06a0a58-974a-419f-a964-b05acdd80eda" />


Los resultados mostraron que no existe una relación directa entre congestión y PIB per cápita. Por ejemplo, Ciudad de México presenta el mayor retraso total (2833 minutos), pero también uno de los PIB per cápita más altos (>20.000 USD), solo superado por Montevideo, que tiene un nivel de congestión muy bajo. La población sí mostró relación con la congestión (ciudades más pobladas → mayor tráfico), pero no con la productividad económica. También se observaron anomalías como Santiago, con alta congestión y un PIB per cápita sorprendentemente bajo.

## 3. Conclusiones y Recomendaciones

El análisis evidencia que el PIB per cápita no es un predictor confiable del nivel de congestión urbana. Uruguay destaca como un caso de alta productividad con tráfico eficiente, mientras que Ciudad de México combina alta congestión con un PIB elevado, lo que sugiere que otros factores —infraestructura, políticas de transporte, planificación urbana— influyen más en la movilidad que la productividad económica.
Santiago aparece como una ciudad prioritaria para inversión en infraestructura de transporte, dado que combina congestión elevada con baja productividad relativa. También se recomienda profundizar en estudios cualitativos y validar fuentes para entender por qué ciudades con niveles similares de desempleo presentan comportamientos tan distintos en movilidad.
En general, los hallazgos sugieren que la región requiere políticas integradas de movilidad urbana y desarrollo económico, y que ciudades como Montevideo podrían servir como benchmark para modelos de tráfico eficiente.
