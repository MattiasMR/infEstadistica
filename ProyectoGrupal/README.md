# Análisis de la Relación entre Contaminación Ambiental y Egresos Hospitalarios en Chile (2018-2024)

## 📋 Descripción del Proyecto

Este proyecto analiza la relación entre la contaminación ambiental (específicamente PM2.5) y la distribución de egresos hospitalarios en Chile durante el período 2018-2024, enfocándose en enfermedades que podrían estar relacionadas con contaminantes ambientales.

## 🎯 Objetivos

- **Objetivo Principal**: Determinar si existe una correlación entre los niveles de contaminación PM2.5 y los egresos hospitalarios por enfermedades relacionadas con contaminación ambiental.

- **Objetivos Específicos**:
  - Analizar la evolución temporal de egresos hospitalarios por zona geográfica
  - Identificar los principales grupos de diagnósticos relacionados con contaminación ambiental
  - Examinar patrones regionales en la distribución de enfermedades
  - Correlacionar datos de contaminación PM2.5 con incidencia de egresos hospitalarios

## 📊 Fuentes de Datos

### Datos de Egresos Hospitalarios
- **Fuente**: DEIS (Departamento de Estadísticas e Información de Salud)
- **Período**: 2018-2024
- **Cobertura**: Nacional, todas las regiones de Chile
- **Formato**: Archivos CSV por año
- **Clasificación**: Códigos CIE-10

### Datos de Contaminación
- **Fuente**: SINCA (Sistema de Información Nacional de Calidad del Aire)
- **Variable**: PM2.5 (Material Particulado 2.5 μm)
- **Período**: 2018-2024
- **Cobertura**: 4 zonas geográficas (Norte, Centro, Sur, Capital)
- **Formato**: Archivos CSV por zona
- **Medición**: Concentraciones diarias en μg/m³

## 🗂️ Estructura del Proyecto

```
ProyectoGrupal/
│
├── README.md                              # Este archivo
├── trabajo_grupal.ipynb                   # Notebook principal con el análisis
├── Diccionario BD egresos hospitalario.xlsx  # Diccionario de códigos CIE-10
├── datos_180101_251108.csv               # Datos adicionales
│
├── Egresos/                              # Datos de egresos hospitalarios
│   ├── EGRESOS_2018.csv
│   ├── EGRESOS_2019.csv
│   ├── EGRESOS_2020.csv
│   ├── EGRESOS_2021.csv
│   ├── EGRESOS_2022.csv
│   ├── EGRESOS_2023.csv
│   └── EGRESOS_2024.csv
│
└── Contaminacion/                        # Datos de contaminación PM2.5
    ├── Norte/
    │   ├── norte1.csv
    │   ├── norte2.csv
    │   ├── norte3.csv
    │   ├── norte4.csv
    │   └── norte5.csv
    ├── Centro/
    │   ├── centro1.csv
    │   ├── centro2.csv
    │   ├── centro3.csv
    │   ├── centro4.csv
    │   ├── centro5.csv
    │   └── centro6.csv
    ├── Sur/
    │   ├── sur1.csv
    │   ├── sur2.csv
    │   ├── sur3.csv
    │   ├── sur4.csv
    │   └── sur5.csv
    └── Capital/
        ├── rm1.csv
        ├── rm2.csv
        ├── rm3.csv
        ├── rm4.csv
        └── rm5.csv
```

## 🔬 Metodología

### 1. Preparación de Datos

#### Filtrado por Códigos CIE-10
Se seleccionaron enfermedades relacionadas con contaminación ambiental según códigos CIE-10:
- **J**: Enfermedades del sistema respiratorio
- **I**: Enfermedades del sistema circulatorio
- **E**: Enfermedades endocrinas, nutricionales y metabólicas
- **C00-D48**: Neoplasias

#### Zonificación Geográfica
Las regiones de Chile se agruparon en 4 zonas:
- **Norte**: Arica y Parinacota, Tarapacá, Antofagasta, Atacama, Coquimbo
- **Centro**: Valparaíso, O'Higgins, Maule, Ñuble, Bíobío
- **Capital**: Región Metropolitana de Santiago
- **Sur**: La Araucanía, Los Ríos, Los Lagos, Aisén, Magallanes

### 2. Análisis Exploratorio

- Distribución temporal de egresos (2018-2024)
- Análisis por sexo, edad y condición de egreso
- Distribución geográfica por región y zona
- Top 10 de grupos de diagnósticos más frecuentes

### 3. Análisis de Contaminación

- Procesamiento de datos PM2.5 por zona y año
- Cálculo de promedios anuales
- Visualización de tendencias temporales

### 4. Análisis de Correlación

- Unión de datos de egresos y contaminación
- Cálculo de correlaciones por zona
- Visualización de relaciones mediante gráficos de dispersión

## 📈 Principales Hallazgos

### Volumen de Datos
- **Total de egresos hospitalarios (2018-2024)**: [Cifra total del análisis]
- **Egresos por enfermedades relacionadas con contaminación**: [Cifra filtrada]
- **Porcentaje de egresos relacionados**: [Porcentaje calculado]

### Distribución Geográfica
- **Región con mayor número de egresos**: Región Metropolitana
- **Zona geográfica más afectada**: [Resultado del análisis]
- **Diferencias regionales significativas**: [Descripción de patrones]

### Evolución Temporal
- **Tendencia general**: [Tendencia observada en el período]
- **Años con mayor incidencia**: [Años identificados]
- **Variaciones estacionales**: [Si se observaron]

### Correlaciones PM2.5 vs Egresos
- **Zona Norte**: [Coeficiente de correlación]
- **Zona Centro**: [Coeficiente de correlación]
- **Zona Sur**: [Coeficiente de correlación]
- **Capital**: [Coeficiente de correlación]

## 📊 Visualizaciones Generadas

El análisis incluye múltiples visualizaciones:

1. **Top 5 Diagnósticos por Zona Geográfica**: Panel de 4 gráficos mostrando los diagnósticos más frecuentes en cada zona durante 2018-2024

2. **Top 5 Diagnósticos Nacionales por Año**: Panel de 7 gráficos mostrando la evolución anual de los principales diagnósticos

3. **Relación PM2.5 vs Egresos con Indicador de Año**: Gráfico de dispersión con:
   - Diferentes marcadores por zona
   - Escala de colores para años
   - Línea de tendencia general
   - Etiquetas de año en cada punto

4. **Evolución Temporal con Doble Eje**: Comparación directa entre:
   - Cantidad de egresos (eje izquierdo)
   - Concentración PM2.5 (eje derecho)

5. **Gráficos de Evolución Temporal**: Tendencias por zona y por los principales grupos de enfermedades

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Pandas**: Manipulación y análisis de datos
- **NumPy**: Operaciones numéricas
- **Matplotlib**: Visualización de datos
- **Seaborn**: Visualización estadística avanzada
- **Jupyter Notebook**: Entorno de desarrollo

## 📋 Requisitos

```python
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
openpyxl>=3.0.0
```

## 🚀 Cómo Ejecutar el Análisis

1. **Clonar/Descargar** el proyecto
2. **Instalar dependencias**:
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl
   ```
3. **Ejecutar el notebook**:
   ```bash
   jupyter notebook trabajo_grupal.ipynb
   ```
4. **Ejecutar celdas secuencialmente** para reproducir todo el análisis

## 📝 Estructura del Notebook

### Sección 1: Carga y Preparación de Datos
- Carga de archivos de egresos (2018-2024)
- Carga del diccionario CIE-10
- Filtrado por códigos de interés
- Mapeo de regiones a zonas

### Sección 2: Análisis Exploratorio de Datos
- Estadísticas descriptivas
- Distribuciones por sexo, edad, condición de egreso
- Análisis temporal y geográfico
- Top 10 diagnósticos nacionales

### Sección 3: Análisis de Contaminación
- Procesamiento de datos PM2.5
- Cálculo de promedios anuales por zona
- Visualización de tendencias

### Sección 4: Análisis de Correlación
- Unión de datasets
- Cálculo de correlaciones por zona
- Visualizaciones de relaciones

### Sección 5: Gráficos Adicionales
- Visualizaciones especializadas
- Gráficos de dispersión con indicadores temporales
- Análisis comparativos

## 🔍 Interpretación de Resultados

### Correlaciones Encontradas
[Descripción de las correlaciones significativas encontradas]

### Implicaciones para la Salud Pública
[Análisis de las implicaciones de los hallazgos]

### Limitaciones del Estudio
- Análisis de correlación, no causalidad
- Datos agregados por zona geográfica
- Posibles factores confusores no considerados
- Período de análisis limitado (7 años)

## 📚 Referencias y Fuentes

- **DEIS**: Departamento de Estadísticas e Información de Salud, Ministerio de Salud de Chile
- **OMS**: Clasificación Internacional de Enfermedades (CIE-10)
- **SINCA**: Sistema de Información Nacional de Calidad del Aire

## 👥 Equipo de Trabajo

- **Mattias Morales**
- **Francisco Polo**
- **Carlos Orellana**



**Última actualización**: Julio 2025

**Versión**: 1.0

**Estado**: Análisis Preliminar
