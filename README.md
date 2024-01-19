# Análisis de Datos de Siniestros Viales en la Ciudad de Buenos Aires

## Descripción del Proyecto

El propósito fundamental de este proyecto es descubrir información relevante que pueda contribuir a la reducción de accidentes mortales en la ciudad de Buenos Aires. Para lograr este objetivo, se llevó a cabo un análisis exhaustivo de los datos suministrados por el Departamento de Transporte, la Subsecretaría de Planificación de Movilidad y la Oficina de Supervisión de Movilidad y Seguridad Vial, abarcando el período comprendido entre 2016 y 2021.

Los datos utilizados para este análisis fueron extraídos de la siguiente fuente: https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales.

## Desarrollo del proyecto

**ETL** : En el transcurso del proceso de ETL, se llevaron registros de casos y víctimas de homicidios y agresiones. En esta fase, se eliminaron columnas irrelevantes, se convirtieron los valores "SD" a nulos, se ajustaron los tipos de datos y se estandarizaron los nombres de columnas y datos. Se adoptó la convención "snake_case", donde todos los nombres se escriben en minúsculas y los espacios se sustituyen por guiones bajos. 

Para acceder a detalles específicos, se puede consultar el notebook [ETL](/Jupiter_Notebooks/ETL.ipynb).

**EDA** : Durante el análisis exploratorio de datos, se identificaron patrones muy interesantes que revelaron información valiosa sobre la naturaleza de los datos.

Para acceder a detalles específicos, se puede consultar el notebook [EDA](Jupiter_Notebooks/EDA.ipynb). 

### Hallazgos

- A lo largo de la mayoría de los años registrados, la comuna con el mayor número de fatalidades suele ser la número 1; no obstante, en el año 2021, la comuna con más fatalidades fue la 4.

- En los accidentes mortales que ocurren en autopistas, la motocicleta es el vehículo de la víctima más frecuente, mientras que en las calles, los peatones son los más afectados.

- Tanto en accidentes fatales como no fatales, la motocicleta es el vehículo de la víctima más común, tanto en autopistas como en calles.

- En promedio, se observa que los accidentes fatales tienden a tener alrededor de 1.03 víctimas, mientras que los accidentes no fatales tienen aproximadamente 1.15 víctimas.

- Las comunas con la menor incidencia de accidentes fatales son la 5 y la 6, mientras que la comuna con menos accidentes no fatales es la 2.

## KPI's

**Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior**

El objetivo es disminuir en un 10% la incidencia de homicidios en accidentes de tráfico durante los últimos seis meses en CABA, en comparación con la tasa de homicidios en accidentes de tráfico del semestre previo. Este indicador se define como el número total de víctimas mortales en el conjunto de datos por cada 100,000 habitantes en una zona geográfica durante un periodo específico.

Para calcular este KPI, se llevó a cabo una comparación entre los últimos dos trimestres de 2021, buscando lograr una reducción del 10% en la tasa de homicidios en accidentes de tráfico.

Durante el último semestre de 2021, la tasa de homicidios en accidentes de tráfico fue de 1.35, indicando una disminución de 0.42, lo que representa una reducción porcentual del -23.64%. Esta reducción implica que se alcanzó con éxito la meta de reducir en un 10% la tasa de accidentes de tráfico en el segundo semestre de 2021.

**Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.**

La cantidad de accidentes mortales de motociclistas en siniestros viales se define como el total de accidentes fatales en los que personas que viajaban en moto resultaron afectadas durante un periodo específico. Para medir la variación en la incidencia de estos accidentes, se utiliza la siguiente fórmula: Restamos el número de accidentes mortales con víctimas en moto del año actual al número correspondiente del año anterior, luego dividimos este resultado entre el número de accidentes mortales con víctimas en moto del año anterior y multiplicamos el cociente por 100.

El incremento del 43.75% en los accidentes de motociclistas durante el año 2021 en comparación con 2020 es una tendencia preocupante que dista considerablemente de la meta establecida de reducir en un 7% los accidentes de motociclistas.

## Esqueleto del Repositorio

- 📂 **Datos**: Aca se encuentran los conjuntos de datos que fueron empleados en el análisis.
    - CSV: Incluye los archivos tras la ejecución del proceso ETL.
    - Originales: Almacena los archivos que fueron descargados inicialmente.

- 📂 **Notebooks**: Contiene el código en Python correspondiente a los pasos llevados a cabo durante el proceso ETL (Extracción, Transformación y Carga) y el análisis exploratorio de datos (EDA).
