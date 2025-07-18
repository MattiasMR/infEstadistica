### Link para informe
https://docs.google.com/document/d/1QxUgAamoS6McOO8df4giphGTtZTzCG6LmPzqlHSFtjs/edit?usp=sharing
# Análisis de Datos de Egresos Hospitalarios (2018-2024)

## Objetivo del Proyecto
Análisis de la relación entre contaminantes ambientales y distribución de egresos hospitalarios en Chile, utilizando datos de egresos hospitalarios del DEIS.

## Estructura del Notebook

### 1. Carga y Preparación de Datos

#### 1.1 Carga de Datos
- **Carga masiva**: Todos los años (2018-2024) se cargan en una sola operación
- **Columna de año**: Se agrega automáticamente basada en el nombre del archivo
- **Encoding**: latin-1 para manejar caracteres especiales chilenos
- **Validación**: Verificación de registros cargados por año

#### 1.2 Diccionario CIE-10
- **Carga del diccionario**: Códigos de clasificación internacional de enfermedades
- **Exploración de columnas**: Verificación de estructura y contenido
- **Validación de capítulos**: Revisión de categorías disponibles

#### 1.3 Filtrado por Códigos de Interés
**Enfermedades relacionadas con contaminación ambiental:**
- **J**: Enfermedades del sistema respiratorio
- **I**: Enfermedades del sistema circulatorio  
- **E**: Enfermedades endocrinas, nutricionales y metabólicas
- **C00-D48**: Neoplasias

#### 1.4 Preparación Final del Dataset
- **Mapeo geográfico**: Regiones agrupadas en Norte, Centro y Sur
- **Códigos de diagnóstico**: Preparación para unión con descripciones
- **Unión con CIE-10**: Incorporación de descripciones de diagnósticos
- **Validación final**: Verificación de integridad y completitud

### 2. Análisis Exploratorio de Datos

#### 2.1 Información General
- **Características del dataset**: Shape, período, distribuciones básicas
- **Demografia**: Distribución por sexo y grupos de edad
- **Condiciones de egreso**: Análisis de resultados hospitalarios
- **Evolución temporal**: Gráfico de tendencia general 2018-2024

#### 2.2 Análisis Geográfico
- **Por región**: Distribución detallada de egresos por las 15 regiones
- **Por zona**: Agrupación Norte-Centro-Sur con visualizaciones
- **Comparativas**: Análisis de diferencias regionales
- **Mapeo territorial**: Visualización de patrones geográficos

#### 2.3 Top 10 Grupos de Diagnósticos
- **Ranking nacional**: Los 10 grupos de enfermedades más frecuentes
- **Agregación inteligente**: Por grupos en lugar de diagnósticos específicos
- **Visualización**: Gráfico de barras con descripciones truncadas
- **Interpretación**: Identificación de patrones epidemiológicos

#### 2.4 Análisis Temporal y Evolutivo
- **Evolución por zona**: Tendencias 2018-2024 para Norte, Centro y Sur
- **Panel comparativo**: 4 gráficos simultáneos (Nacional + 3 zonas)
- **Top 3 grupos**: Seguimiento de los principales grupos de enfermedades
- **Análisis de tendencias**: Identificación de patrones de crecimiento/decrecimiento

## Características Técnicas

### Variables Clave del Dataset
- **`df_completo`**: Todos los egresos hospitalarios 2018-2024 (~millones de registros)
- **`df_filtrado`**: Solo enfermedades relacionadas con contaminación ambiental  
- **`df_final`**: Dataset completo con descripciones CIE-10 y zonas geográficas mapeadas

### Visualizaciones Incluidas
- **Gráficos temporales**: Evolución año a año con múltiples series
- **Gráficos comparativos**: Barras para rankings y distribuciones
- **Panel de análisis**: Visualizaciones simultáneas 2x2 por zona
- **Mapas conceptuales**: Distribución geográfica Norte-Centro-Sur

## Próximos Pasos Sugeridos
- Análisis estadístico inferencial (correlaciones, tests)
- Modelado predictivo de tendencias
- Análisis de series temporales avanzado
- Incorporación de variables socioeconómicas
- Análisis de causalidad con datos ambientales
