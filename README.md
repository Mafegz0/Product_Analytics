# Product Analytics | Inteligencia competitiva de educación superior

Proyecto de **analítica de mercado para la oferta académica**, orientado a apoyar decisiones de portafolio, posicionamiento y precios mediante el análisis de programas, instituciones y demanda histórica.

**Estado:** en desarrollo. El repositorio publica las primeras tres fases de la metodología **ASUM-DM**; el modelo BI, la evaluación y el despliegue se documentarán a medida que se desarrollen.

## Problema de negocio y objetivo

Se requiere comparar la oferta de programas académicos de distintas instituciones y relacionar sus características con información histórica de matrícula para respaldar decisiones sobre:

- Programas e instituciones comparables.
- Modalidades y duración de los programas.
- Posicionamiento competitivo, precios y descuentos, cuando estén disponibles las fuentes comerciales.
- Evolución de la demanda y oportunidades de portafolio.

**Objetivo de esta etapa:** preparar una base SNIES consistente y analizable para el periodo **2020–2025**, homologando estructuras de origen y desarrollando un análisis exploratorio y dimensiones para la comparación de programas.

> **Alcance de fuentes:** el histórico SNIES es la base trabajada en los notebooks publicados. El análisis de precios, descuentos y propuesta de valor requiere otras fuentes y corresponde a fases posteriores. No se presenta como un resultado ya implementado.

## Arquitectura objetivo

- **Fuentes:** histórico SNIES (2020–2025) y, en etapas posteriores, fuentes de oferta y precios.
- **Preparación:** Python/pandas para lectura, revisión del esquema, normalización de nombres y tipos de columnas, consolidación histórica y creación de dimensiones.
- **Consumo previsto:** modelo analítico y tablero de inteligencia competitiva en Power BI.

La consolidación debe preservar el año de origen y atender las diferencias de columnas entre periodos, especialmente en 2020–2022. La variable **MATRICULADOS PRIMER CURSO** se contempla en las reglas de homologación histórica.

## Metodología ASUM-DM: avance documentado

| Fase | Estado documental | Evidencias en el repositorio |
| --- | --- | --- |
| **01 · Business Understanding** | Documentada | Carta de proyecto, RACI, matriz de riesgos, Decision Log y README |
| **02 · Data Understanding** | Documentación parcial | README y especificación YAML de reglas de calidad del histórico SNIES |
| **03 · Data Preparation** | Notebook publicado | Normalización del histórico, EDA y trabajo sobre dimensiones |
| **04 · Modeling** | Pendiente | Modelo analítico y visualizaciones por desarrollar/documentar |
| **05 · Evaluation** | Pendiente | Conciliaciones, métricas y validaciones por documentar |
| **06 · Deployment** | Pendiente | Publicación, manuales y operación por documentar |

La existencia de **reglas de calidad declaradas** no implica que su ejecución automática ni sus resultados hayan sido comprobados.

## Estructura actual del repositorio

```text
Product_Analytics/
├── 01_Business_Understanding/
│   ├── Project_Charter.xlsx
│   ├── RACI.xlsx
│   ├── Risk_Matrix.xlsx
│   ├── Decision_log.md
│   └── README.md
├── 02_Data_Understanding/
│   ├── data_quality_rules_SNIES.yaml
│   └── README.md
├── 03_Data_Preparation/
│   └── notebooks/
│       └── 01_SNIES_Normalizacion_EDA_Dimensiones.ipynb
├── .gitignore
└── README.md
```

Las carpetas **04_Modeling**, **05_Evaluation** y **06_Deployment** se incorporarán conforme avance el proyecto. El inventario y diccionario de datos, aunque previstos en la metodología, todavía no figuran publicados como archivos independientes.

## Documentación y artefactos

- [01 · Business Understanding](01_Business_Understanding/README.md)
- [Registro de decisiones](01_Business_Understanding/Decision_log.md)
- [02 · Data Understanding](02_Data_Understanding/README.md)
- [Reglas de calidad SNIES](02_Data_Understanding/data_quality_rules_SNIES.yaml)
- [Notebook principal: SNIES 2020–2025](03_Data_Preparation/notebooks/01_SNIES_Normalizacion_EDA_Dimensiones.ipynb)

## Herramientas y prácticas

**Python, pandas, Jupyter Notebook, Excel, YAML, Git y GitHub**; metodología **ASUM-DM**. **Power BI** es la herramienta prevista para la visualización ejecutiva.

## Gestión de datos

El archivo `.gitignore` excluye, entre otros, archivos de datos (`.xlsx`, `.csv`) y de Power BI (`.pbix`). Los entregables de gestión ya incorporados al historial del repositorio pueden seguir versionados: `.gitignore` no elimina archivos previamente cargados.

**Responsable técnico:** Coordinación de Analítica de Negocio y Riesgos.
