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


#  Dataset utilizado
- https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/-ndice-de-precios-de-insumos-agr-colas/gwbi-fnzs/about_data

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
git clone https://github.com/jeffersoncordobap/proyecto_UPRA.git

# Documentación

## Historias de Usuario del Proyecto UPRA

# HU01 – Limpieza inicial de datos
Como analista de datos del proyecto,
quiero cargar el dataset original en un Jupyter Notebook y verificar tipos de datos, vacíos, duplicados y rangos,
para asegurar que la base esté limpia antes de hacer el análisis en Power BI.

Criterios de aceptación:
El notebook carga correctamente el dataset.
Se detectan y documentan valores missing.
No existen duplicados.
Todas las columnas numéricas están en formato numérico.
La columna fecha está en formato datetime.

# HU02 – Normalización y estandarización
Como analista,
quiero normalizar nombres de columnas y limpiar valores erróneos,
para asegurar consistencia en la base final.

Criterios:

Todas las columnas tienen nombres claros y consistentes.
Se eliminaron caracteres extraños (comas, guiones, espacios).
No hay columnas con mezcla de tipos.


# HU03 – Crear columnas derivadas
Como analista,
quiero generar nuevas columnas como fecha, año, mes, mes_nombre, insumo, indice, categoria
para facilitar el análisis en Power BI.

Criterios:

Existe columna fecha
Existe columna año
Existe columna mes
Existe columna mes_nombre
Existe columna insumo
Existe columna indice
Existe columna categoria

HU04 – Exportar dataset limpio
Como desarrollador del equipo,
quiero exportar el dataset limpio en formato CSV,
para usarlo en Power BI sin transformaciones adicionales.

Criterios:
Archivo exportado: insumos_clean.csv
No existen valores no numéricos en campos numéricos.


# HU05 – Cargar el dataset a Power BI

Como visualizador/dashboards,
quiero cargar el dataset limpio en Power BI,
para comenzar a diseñar las visualizaciones.

Criterios:
Se conecta el CSV con éxito.
No se requieren transformaciones adicionales en Power Query.
Power BI reconoce las columnas de fechas correctamente.


# HU06 – Visualización de tendencia general

Como usuario final, 
quiero ver la evolución del índice total de insumos agrícolas,
para identificar tendencias generales del mercado.

Criterios:
Gráfico de línea del índice total por fecha.
Filtro por año.



# HU07 – Análisis por categorías (fertilizantes, plaguicidas, otros)
Como usuario,
quiero visualizar el comportamiento individual de las categorías,
para comparar crecimientos.

Criterios:
Líneas comparativas por categoría.
Selección por rango de fechas.


# HU08 – Ranking de variación anual
Como analista,
quiero un ranking de insumos con mayor variación anual,
para identificar cuáles han crecido más en precio.

Criterios:
Gráfico de barras ordenado de mayor a menor variación.
Selección del año.


# HU9 – Identificación de picos inflacionarios
Como usuario,
quiero visualizar meses/años con mayores aumentos,
para detectar periodos críticos.

Criterios:
Heatmap (variación mensual) o gráfico de puntos.
Indicadores de máximos.


# HU10 - Identificar la tasa de variacion anual compuesta

Como analista, 
quiero obtener los datos de la grafica de TCAC
para obtener los datos de crecimiento y decrecimiento en periodos de tiempo. 

# HU11 - Identificar año con mayor inflacion

Como analista,
quiero obtener el año donde el promedio del índice de un insumo (o del total) es mayor,
para identificar el periodo en el que ese insumo presentó su comportamiento más crítico y tomar decisiones basadas en esa variación.

# HU12 - El insumo con mayor aumento en un periodo

Como analista, 
quiero obtener el insumo con mayor aumento en un periodo de tiempo
para encontrar posibles causas y como contrarestarlo. 

# HU13 - El insumo con mayor disminucion en un periodo 

Como analista, 
quiero obtener el insumo con menor aumento en un periodo de tiempo, 
para conocer momentos donde seria mas rentable comprarlos. 

# HU13 - Filtrado de informacion 

Como usuario, 
quiero poder filtrar la informacion por años, categorias o insumos segun sea el caso, 
para poder observar la informacion mas facilmente.

# HU14 - Borrar todos los filtros

Como usuario, 
quiero poder eliminar todos las casillas seleccionadas de los filtros 
para faciltar el analisis. 

# HU15 - Busquedad inteligente

Como usuario, 
quiero poder buscar informacion util de acuerdo a los datos de la grafica, 
para complementar mi conomiento. 

# HU16 - Diseño intuitivo 

Como analista, 
quiero que las graficas suministradas sean faciles de entender, 
para ahorrar tiempo en la estapa de analisis. 

# HU17 - Descripcion de paginas

Como usuario, 
Quiero una seccion de ayuda, 
Para aumentar la facilidad de comprencion. 
