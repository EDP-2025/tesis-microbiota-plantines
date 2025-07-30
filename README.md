# Proyecto de Título: Modelos Mixtos para Microbiota y Plantines

**Autora:** Gabriela Gutiérrez  
**Fecha:** Julio 2025  
**Repositorio:** https://github.com/EDP-2025/tesis-microbiota-plantines

---

## Descripción

Este repositorio contiene los scripts en RMarkdown utilizados en la memoria de pregrado de Ingeniería Civil Matemática en la Universidad de Valparaíso.  
Se incluyen dos estudios principales:

- **Microbiota vaginal:** Modelos NBMM y ZINBMM para caracterizar la dinámica longitudinal en mujeres gestantes vs. no gestantes.  
- **Crecimiento de plantines:** Modelos mixtos lineales (LMM) para evaluar la evolución del diámetro del ancho del cuello de plantines bajo distintos tratamientos.

---

## Estructura del repositorio

```plaintext
tesis-microbiota-plantines/
├── README.md
├── microbiota/
│   └── microbiota.Rmd                ← Análisis y resultados microbiota
└── plantines/
    ├── plantines.Rmd                 ← Script principal de modelado de crecimiento
    ├── variables_ambientales_acumuladas.Rmd
    │   → Lee `RedMeteo.xlsx` (datos ambientales)
    │     y genera `env_acumulado_plantas.xlsx`
    ├── Medicion_plantines.xlsx       ← Mediciones de altura y DAC de los plantines
    └── env_acumulado_plantas.xlsx    ← Salida de `variables_ambientales_acumuladas.Rmd`,
        usada en `plantines.Rmd` para incorporar covariables ambientales

---
## Detalles carpeta `plantines/`

- `variables_ambientales_acumuladas.Rmd`:  
  Proceso completo de lectura de `RedMeteo.xlsx`, cálculo de variables ambientales acumuladas (temperatura, radiación, lluvia, etc.) para las fechas de medición y generación de `env_acumulado_plantas.xlsx`.

- `plantines.Rmd`:  
  Análisis de crecimiento de plantines mediante modelos mixtos lineales, empleando como covariables ambientales el archivo resultante `env_acumulado_plantas.xlsx` y las mediciones de altura y diámetro en `Medicion_plantines.xlsx`.



