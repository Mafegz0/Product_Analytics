# Product Analytics – Modelo BI Competencia

Repositorio técnico para el diseño e implementación de un modelo analítico de inteligencia competitiva, enfocado en la construcción de una vista ejecutiva para el análisis de:

- Oferta académica comparable.
- Competencia directa por programa.
- Precios y descuentos.
- Modalidad y duración.
- Diferenciales de la oferta académica.
- Evolución histórica de la demanda.
- Posicionamiento competitivo precio–valor.
- Tendencias de matrícula.
- Oportunidades y brechas de portafolio.

El proyecto está orientado a consolidar y estandarizar información competitiva proveniente de diferentes fuentes, mejorando la comparabilidad, calidad, trazabilidad y oportunidad de los datos utilizados para soportar decisiones de precio, portafolio, posicionamiento y captación.

La solución analítica será implementada mediante un modelo de datos y un dashboard ejecutivo en Power BI.

---

## Objetivos del Proyecto

- Consolidar la información financiera en un modelo único.
- Estandarizar precios, descuentos, vigencias y demás variables comerciales necesarias para realizar comparaciones válidas.
- Integrar los últimos cinco años disponibles de información histórica de matrículas provenientes de fuentes oficiales.
- Relacionar variables de precio, propuesta de valor, características de la oferta y comportamiento histórico de la demanda.
- Construir un dashboard estratégico en Power BI.
- Documentar reglas de negocio y transformación de datos.

---

## Arquitectura General

El proyecto se estructura en dos capas principales:

### Data Layer
- Fuentes en Excel
- Transformaciones y homologaciones
- Creación de variables calculadas
- Definición de llaves y granularidad

### BI Layer
- Modelo en Power BI
- Medidas DAX 
- Filtros y vistas por programa.
- Comparativos de oferta.
- Análisis de precios.
- Tendencias históricas de matrícula.
- Visualizaciones de posicionamiento competitivo.
- Análisis precio–valor.

---

## Metodología

El proyecto sigue el enfoque ASUM-DM estructurado en 6 fases:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

Cada fase cuenta con documentación formal y entregables definidos.
---

## Estructura del Repositorio
```
Credito-y-Cartera/
│
├── 01_Business_Understanding/
│   ├── Project_Charter.xlsx
│   ├── Risk_Register.xlsx
│   ├── Stakeholders_RACI.xlsx
│   ├── Decision_Log.md
│   └── README.md
│
├── 02_Data_Understanding/
│   ├── data_inventory.xlsx
│   ├── data_dictionary.xlsx
│   ├── data_quality_rules.yaml
│   └── README.md
│
├── 03_Data_Preparation/
│   ├── PowerQuery_Transformations.md 
│   ├── Reglas_Transformacion.xlsx
│   └── README.md
│
├── 04_Modeling/
│   ├── Modelo_Dimensional.png
│   ├── Modelo_Descripcion.md
│   └── README.md
│   ├── visualization/      
│         ├── Medidas_DAX.xlsx
│         ├── KPIs_Definicion.md
│         ├── Tablas_Calculadas.md
│
├── 05_Evaluation/
│   ├── validation_report.md
│
├── 06_Deployment/
│   ├── powerbi/
│   ├── Manual_de_usuario.pdf
│
├── Data/
│
├── .gitignore
└── README.md

```

---

## Stack técnico
- Microsoft Excel
- Power BI
- Git & GitHub

## Alcance técnico

Incluye:

- Identificación y documentación de fuentes de información.
- Inventario de datos.
- Homologación de programas.
- Normalización de variables competitivas.
- Normalización de precios y descuentos.
- Integración de información histórica de demanda..
- Definición de criterios de competencia directa.
- Modelado dimensional.
- Construcción de métricas de inteligencia competitiva.

No incluye:

- Desarrollo de modelos predictivos de matrícula.
- Predicción automática de demanda.
- Precios en tiempo real.
- Ejecución automática de decisiones comerciales.
- Modificación automática de precios.
- Automatización completa de fuentes cuando técnicamente no se encuentre disponible.

##  Responsable técnico

Coordinadora de Analítica de negocio y riesgos 