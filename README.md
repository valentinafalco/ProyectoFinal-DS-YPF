# ProyectoFinal-DS-YPF
## Grupo 17 - Fundación YPF - Ingenias+
### Introducción
Este trabajo analiza cómo funcionaron los hospitales de la Provincia de Buenos Aires entre 2005 y 2022, el detalle del rendimiento de los establecimientos teniendo en cuenta la información de: cantidad de consultas odontológicas, médicas y paramédicas, interconsultas, egresos, camas disponibles, días de estadía, etc. A partir de datos oficiales, se observa el rendimiento de distintos centros de salud en cada municipio y región sanitaria. 

### Objetivo
---
El objetivo es entender mejor cómo evolucionó el sistema hospitalario en ese período, identificar patrones, analizar diferencias entre zonas y analizar posibles mejoras a futuro. 
Realizaremos una exploración, limpieza y modelado de los datos, con el fin de generar conclusiones accionables y visualizaciones interactivas que faciliten la comprensión de los resultados por parte de tomadores de decisiones.

### Integrantes 
Trabajo realizado por el Grupo 17 del curso de Ciencia de Datos de Fundación YPF, como parte del programa Ingenias+, una iniciativa que tiene como objetivo promover la participación de más mujeres en el ámbito de la programación.
- Falco Valentina - Analista de Datos, Estudiante de Ingeniería en Sistemas
- Flores Lorena - Ingeniera en Sistemas

### Dataset
- Rendimiento de Establecimientos de Salud (2005-2022) - Datos Abiertos de la Provincia de Buenos Aires: https://catalogo.datos.gba.gob.ar/th/dataset/rendimientos-establecimientos-salud/archivo/8c3130cb-61ad-4014-b829-503b214ba3c0

### Entregables:
- Notebook con análisis exploratorio (correspondiente a pre-entrega 2): (https://github.com/valentinafalco/ProyectoFinal-DS-YPF/blob/4c6e5da3ef178f3e92d463698c91f780a630b259/2da%20Entrega/2daEntrega.ipynb)
- Notebooks donde apliquen modelos de aprendizaje supervisado y no supervisado y donde se observen resultados obtenidos (correspondientes a pre-entrega 3 y 4): https://github.com/valentinafalco/ProyectoFinal-DS-YPF/blob/4c6e5da3ef178f3e92d463698c91f780a630b259/3era%20Entrega/3raEntrega.ipynb // https://github.com/valentinafalco/ProyectoFinal-DS-YPF/tree/4c6e5da3ef178f3e92d463698c91f780a630b259/4ta%20Entrega

### Metodología
#### Análisis Exploratorio - Pre-entrega 2
**Preprocesamiento:** Se trabajó con datos oficiales de la Provincia de Buenos Aires (2005-2022). Se realizó imputación de valores nulos según la distribución de cada variable (media o mediana) y se escaló para mejorar el rendimiento de los modelos.

**Agrupación de variables:** Se organizaron en tres grandes grupos:
- Atención Ambulatoria (consultas médicas, odontológicas, etc.).
- Internación (camas disponibles, días de estadía, ocupación, etc.).
- Resultados Sanitarios (egresos, defunciones, tasa de mortalidad).

**Tendencias:** Se visualizaron cambios en los egresos, consultas y mortalidad, especialmente antes y después de la pandemia.

#### Modelos de Aprendizaje Supervisado - Pre-entrega 3
- Regresión lineal: Se estudió la relación entre variables como pacientes_dias y dias_estadia, obteniendo una alta correlación (R² ≈ 0.96). Esto permitió entender mejor el uso de recursos hospitalarios.

- Modelado de series temporales (Prophet): Se pronosticó la evolución de los egresos hospitalarios a futuro. El modelo predice una tendencia creciente, útil para planificación estratégica.

- Evaluación: Se utilizaron métricas como MAE, MSE, RMSE y R², con buenos resultados en ambos modelos.

#### Modelos de Aprendizaje No Supervisado - Pre-entrega 4
- Clustering con K-Means: Se identificaron 3 perfiles de establecimientos para cada grupo de variables: Baja, media y alta complejidad o volumen de atención.

- Evaluación con Silhouette Score: Valores altos (hasta 0.92) indicaron una buena separación entre clústeres.

- DBSCAN: Se aplicó para detectar outliers y agrupaciones densas sin predefinir la cantidad de clústeres. Permitió identificar establecimientos atípicos o con características particulares, como centros especializados o de baja eficiencia.

