# 02 — Data Understanding | Histórico SNIES 2020–2025

## Objetivo de la fase

Comprender la estructura, el alcance y la calidad de las fuentes **SNIES** utilizadas para el análisis de mercado de programas académicos y educación superior en Colombia.

El foco actual es el histórico **2020–2025** y su consolidación para permitir comparaciones entre instituciones, programas, modalidades y matrícula de primer curso.

## Fuente y unidad de análisis

- **Fuente de trabajo:** histórico SNIES, organizado por año (2020, 2021, 2022, 2023, 2024 y 2025).
- **Unidad reportada:** registro histórico de un programa académico asociado a una institución, según la estructura y granularidad del archivo fuente.
- **Variables relevantes:** código de la institución, programa, año de origen, modalidad y matriculados de primer curso, entre otras.
- **Consideración:** el esquema de 2020 y las denominaciones de varios campos difieren de los años posteriores; no se debe asumir comparabilidad automática.

## Actividades documentadas

1. Inspección y comparación de hojas y columnas por año.
2. Identificación de campos ausentes y nombres equivalentes.
3. Definición de un esquema común para concatenar los periodos.
4. Revisión de códigos de instituciones, periodos y atributos de programas.
5. Identificación de reglas para preservar procedencia y trazabilidad.
6. Evaluación exploratoria y dimensionamiento de programas en el notebook de preparación.

## Reglas de calidad de datos

El artefacto [data_quality_rules_SNIES.yaml](data_quality_rules_SNIES.yaml) define expectativas para cada anualidad y el histórico consolidado, incluyendo:

- **Completitud:** presencia de códigos de instituciones y periodos.
- **Validez:** formatos y dominios permitidos.
- **Consistencia:** correspondencias entre nombres históricos de variables, como METODOLOGÍA y MODALIDAD.
- **Exactitud:** coherencia entre año de fuente y año de origen.
- **Integridad referencial y unicidad:** controles previstos para cruces y dimensiones.

Las reglas contienen identificadores y niveles de severidad. **Se trata de especificaciones documentadas:** su existencia no demuestra que todas se hayan ejecutado o que sus resultados hayan sido aprobados.

## Entregables publicados

- [Reglas de calidad SNIES — YAML](data_quality_rules_SNIES.yaml)
- [Notebook de normalización, EDA y dimensiones (fase 03)](../03_Data_Preparation/notebooks/01_SNIES_Normalizacion_EDA_Dimensiones.ipynb)

**Pendientes de publicación en esta fase:** inventario de fuentes y diccionario de datos como documentos independientes. No se anuncian como entregables ya disponibles.

## Transición a Data Preparation

Los hallazgos de diferencias de columnas, tipos y semántica alimentan la normalización del histórico 2020–2025 desarrollada en **03_Data_Preparation**. La integración posterior de datos comerciales de precios y descuentos forma parte del alcance futuro del proyecto.
