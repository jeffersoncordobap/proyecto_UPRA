#  Proyecto UPRA – Análisis del Índice de Precios de Insumos Agrícolas en Colombia

Herramienta analítica que permite visualizar la evolución histórica del **índice de precios de insumos agrícolas en Colombia**, facilitando la toma de decisiones informadas en el sector agropecuario.

---

##  Descripción del proyecto

Este proyecto desarrolla una solución completa para el análisis, limpieza y visualización del índice de precios de insumos agrícolas publicados por la **Unidad de Planificación de Tierras Rurales, Adecuación de Tierras y Usos Agropecuarios (UPRA)**.

Incluye:

- Procesamiento y normalización del dataset original.
- Transformación a un formato analítico apto para Power BI.
- Construcción de visualizaciones para estudiar tendencias, variaciones anuales y cambios significativos.

---

##  Objetivo general

Crear una **visualización interactiva** del comportamiento del índice de precios de insumos agrícolas para identificar tendencias, variaciones anuales y períodos de incremento significativo.

---

##  Objetivos específicos

- **OE1.** Analizar la variación del índice por tipo de insumo en el periodo disponible.  
- **OE2.** Generar visualizaciones (líneas, barras y ranking) sobre las tendencias del mercado.  
- **OE3.** Identificar meses/años con mayores incrementos o tendencias inflacionarias persistentes.  

---

##  Impacto esperado

- Facilita decisiones de compra de insumos.
- Mejora procesos de negociación y planificación técnica.
- Apoya la asistencia agropecuaria.
- Aumenta la competitividad del pequeño agricultor.

---

#  Estructura del repositorio
data/
    insumos_raw
    insumos_clean
notebooks/
    UPRA_limpieza_notebook.ipynb
powerbi/
    dashboard.pbix

README.md

Estructura insumos_clean:

| fecha | año | mes | mes_nombre | insumo | indice | categoria |
|------|-----|-----|-------------|--------|--------|-----------|

---

#  Tecnologías utilizadas

- Python (pandas, numpy)  
- Jupyter Notebook  
- Power BI  
- Git / GitHub  

---

#  Cómo ejecutar este proyecto

### 1. Clonar el repositorio
```bash
git clone https://github.com/jeffersoncordobap/proyecto_UPRA.git

