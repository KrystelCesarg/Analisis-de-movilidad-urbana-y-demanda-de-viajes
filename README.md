# Eficiencia Operativa y Fuerza Laboral: Impacto Climático en la Duración de Trayectos

## 🎯 Problema de Negocio
Para una empresa de transporte como Zuber, que busca expandirse en la ciudad de Chicago, entender los patrones de movilidad urbana y los factores externos impredecibles es fundamental para gestionar la oferta de conductores y diseñar tarifas dinámicas confiables. Este proyecto cuantifica el impacto de las condiciones climáticas adversas en la duración de los viajes y mapea las zonas de mayor demanda para optimizar la distribución de la flota.

## 📊 Conjunto de Datos
Los datos fueron extraídos mediante consultas SQL y analizados en Python utilizando tres conjuntos de datos:
* **Dataset 1 (Empresas):** Nombres de las compañías de taxis y volumen total de viajes realizados.
* **Dataset 2 (Destinos):** Barrios de destino y promedio de viajes finalizados.
* **Dataset 3 (Viajes Loop → O'Hare):** Registros de fecha/hora, condiciones climáticas categorizadas y duración exacta del viaje en segundos.

## 🔍 Análisis y Metodología
1. **Validación de Calidad de Datos:** Auditoría de valores ausentes, eliminación de registros duplicados, conversión de tipos de datos y reformateo de variables temporales.
2. **Análisis Exploratorio de Datos (EDA):** Identificación de la concentración del mercado entre los líderes de la industria y mapeo de los puntos críticos (*hotspots*) de finalización de viajes.
3. **Prueba de Hipótesis Estadística:** Implementación de una prueba t de Student para muestras independientes ($\alpha = 0.05$) para evaluar si la duración promedio de los viajes cambia significativamente durante los sábados lluviosos en comparación con días de clima favorable.

## 💡 Hallazgos Clave
* **Alta Concentración de Mercado:** El ecosistema de transporte está altamente concentrado en un grupo reducido de empresas líderes, con Flash Cab encabezando el volumen de viajes.
* **Zonas de Alta Movilidad:** Los viajes se concentran drásticamente en distritos comerciales, financieros y turísticos: Loop, River North, Streeterville y West Loop.
* **Impacto Cuantificable del Clima:** El clima lluvioso incrementa significativamente el tiempo de traslado.
  * Promedio en clima favorable: 1,999.68 segundos (~33 minutos).
  * Promedio en clima lluvioso: 2,427.21 segundos (~40 minutos).
  * La diferencia promedio es de aproximadamente 7 minutos, validada estadísticamente con un estadístico $t = -6.95$ y un $p\text{-value} < 0.05$, lo que permitió rechazar la hipótesis nula.

## 🚀 Recomendaciones Estratégicas
* **Planificación Dinámica de Turnos de la Fuerza Laboral:** Utilizar la métrica del impacto climático (~7 minutos de retraso promedio) para ajustar automáticamente los turnos de los conductores y los intervalos de despacho en días lluviosos. Esto ayuda a prevenir el agotamiento de los conductores (*burnout*) y mantiene los niveles de satisfacción del cliente.
* **Incentivos Geofocalizados para Conductores:** Implementar tarifas dinámicas o bonos para los conductores en los 4 barrios comerciales principales durante las horas pico, asegurando que la oferta de personal coincida con la alta demanda de movilidad urbana.

## 🛠️ Herramientas y Tecnologías
* **Lenguajes y Entornos:** SQL, Python 3.
* **Librerías:** Pandas, NumPy, Matplotlib, SciPy (Análisis Estadístico Avanzado).
