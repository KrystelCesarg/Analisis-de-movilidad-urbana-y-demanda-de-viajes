# 🚕 Análisis de Mercado para Zuber en Chicago

## 📌 Descripción del proyecto

Zuber es una empresa de transporte compartido que busca expandirse en la ciudad de Chicago. El objetivo de este proyecto es identificar patrones en los viajes de taxi, comprender las preferencias de los pasajeros y analizar cómo factores externos, como las condiciones climáticas, afectan la duración de los trayectos.

El proyecto combina resultados obtenidos mediante consultas SQL con análisis exploratorio y pruebas estadísticas realizadas en Python.

---

## 🎯 Objetivos

* Analizar la actividad de las principales compañías de taxis.
* Identificar los barrios con mayor número de finalizaciones de viaje.
* Explorar patrones de movilidad urbana en Chicago.
* Evaluar el impacto de las condiciones climáticas sobre la duración de los viajes.
* Validar estadísticamente una hipótesis mediante una prueba t de Student.

---

## 🗂️ Conjunto de datos

Los datos utilizados fueron obtenidos mediante consultas SQL realizadas en un entorno de base de datos y exportados posteriormente a archivos CSV para su análisis.

### Dataset 1: Empresas de taxis

* `company_name`: nombre de la empresa.
* `trips_amount`: número total de viajes realizados.

### Dataset 2: Destinos de viaje

* `dropoff_location_name`: barrio de destino.
* `average_trips`: promedio de viajes finalizados.

### Dataset 3: Viajes Loop → O'Hare

* `start_ts`: fecha y hora de inicio.
* `weather_conditions`: condiciones climáticas.
* `duration_seconds`: duración del viaje.

---

## 🛠️ Herramientas utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy
* Jupyter Notebook
* SQL (consultas realizadas en entorno académico)

---

## 🔎 Metodología

### 1. Preparación de datos

* Validación de tipos de datos.
* Revisión de valores ausentes.
* Identificación de registros duplicados.
* Conversión de variables temporales.

### 2. Análisis exploratorio

* Identificación de las compañías con mayor número de viajes.
* Identificación de los principales destinos de la ciudad.
* Visualización de patrones mediante gráficos.

### 3. Prueba de hipótesis

Se evaluó la siguiente hipótesis:

**H₀:** La duración promedio de los viajes desde Loop hasta el Aeropuerto Internacional O'Hare no cambia durante los sábados lluviosos.

**H₁:** La duración promedio de los viajes desde Loop hasta el Aeropuerto Internacional O'Hare cambia durante los sábados lluviosos.

Se utilizó una prueba t de Student para muestras independientes con un nivel de significancia de α = 0.05.

---

## 📊 Principales hallazgos

### Empresas de taxi

* Flash Cab fue la compañía con mayor número de viajes registrados.
* El mercado presenta una alta concentración en un grupo reducido de empresas líderes.

### Destinos principales

Los barrios con mayor promedio de finalizaciones fueron:

1. Loop
2. River North
3. Streeterville
4. West Loop

Estos resultados sugieren una alta concentración de movilidad en zonas comerciales, turísticas y de negocios.

### Impacto del clima

Los viajes realizados durante condiciones lluviosas presentaron una duración promedio superior a los realizados en condiciones favorables.

**Duración promedio:**

* Clima favorable: 1,999.68 segundos
* Clima lluvioso: 2,427.21 segundos

**Diferencia promedio:** aproximadamente 7 minutos.

La prueba estadística arrojó:

* Estadístico t = -6.95
* p-value < 0.05

Por lo tanto, se rechazó la hipótesis nula y se concluyó que las condiciones climáticas influyen significativamente en la duración de los viajes.

---

## 📈 Resultados

El análisis permitió identificar patrones relevantes sobre la operación del mercado de taxis en Chicago y demostrar cómo factores externos, como la lluvia, afectan los tiempos de traslado.

Estos hallazgos pueden ser utilizados para comprender mejor la demanda de transporte urbano y optimizar la planificación operativa de servicios de movilidad.

---

## 📊 Visualizaciones

### Top 10 empresas de taxi
![Empresas]<img width="1027" height="885" alt="Top 10 empresas de taxis" src="https://github.com/user-attachments/assets/f70ee676-cee5-4fd2-8c63-6c58424bb187" />


### Top 10 barrios por finalización de viajes
![Barrios]<img width="1027" height="815" alt="Top 10 barrios principales" src="https://github.com/user-attachments/assets/f4254d4d-d70c-4572-bab1-985e2ed82293" />


## 🚧 Retos encontrados y aprendizajes

Este proyecto representó una oportunidad para conectar distintas etapas del análisis de datos, desde la obtención de información hasta la generación de conclusiones respaldadas por evidencia estadística.

Uno de los principales retos fue comprender el contexto de los datos y traducir una pregunta de negocio en un análisis estructurado. Más allá de ejecutar código, fue necesario interpretar qué información aportaba cada conjunto de datos y cómo podía contribuir a responder los objetivos del proyecto.

Durante el análisis exploratorio aprendí la importancia de revisar cuidadosamente la calidad de los datos antes de comenzar cualquier análisis. Verificar tipos de datos, identificar valores ausentes y revisar posibles duplicados permitió trabajar con mayor confianza en los resultados obtenidos.

Otro aprendizaje importante fue la interpretación de visualizaciones. Crear gráficos es relativamente sencillo, pero extraer conclusiones relevantes para el negocio requiere observar patrones, comparar resultados y contextualizar la información.

Finalmente, la parte más enriquecedora fue la prueba de hipótesis. Este proyecto me permitió reforzar conceptos estadísticos y comprender cómo utilizar herramientas analíticas para responder preguntas reales. Más allá de obtener un valor p, aprendí a interpretar los resultados y comunicar conclusiones de manera clara y fundamentada.

En conjunto, este proyecto fortaleció mis habilidades en análisis exploratorio de datos, visualización, estadística aplicada y comunicación de hallazgos, además de mostrarme cómo cada etapa del proceso analítico contribuye a la toma de decisiones basada en datos.

## 👩‍💻 Autor

**Krystel C. Garcia**

Proyecto desarrollado como parte de la formación en Análisis de Datos, aplicando técnicas de SQL, análisis exploratorio, visualización de datos y pruebas estadísticas.
