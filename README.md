# Clarillo Predice

Proyecto de Aprendizaje + Servicio (A+S) de la asignatura Taller de Analítica Predictiva y Prescriptiva (IDA602), AIEP.

Herramienta para anticipar cuándo y dónde es más probable que se inicie un incendio forestal en el entorno de 25 km del
Parque Nacional Río Clarillo (Pirque, Región Metropolitana). Socio comunitario: guardaparque del parque (CONAF).

## Contenido

| Archivo | Descripción |
|---|---|
| `Clarillo_Predice_AS.ipynb` | datos, análisis exploratorio, modelo de días críticos, ranking de variables, mapa de prioridad y boletín semanal con pronóstico de 7 días |
| `dataset_incendios_pirque_diario.csv` | un día por fila (julio 2002 a junio 2025) con la variable objetivo y 36 variables de clima, índices de CONAF, calendario e incendios previos |
| `incendios_entorno.csv` | 888 incendios a 25 km o menos del parque, con fecha, comuna, causa, superficie y celda |
| `celdas_entorno.csv` | 484 celdas de 2 x 2 km del entorno, con relieve, vegetación, caminos y edificaciones |

## Fuentes

CONAF (registro histórico de incendios en Datos para Resiliencia y capas SIMEF), Open-Meteo (reanálisis ERA5),
DGA (estación Pirque, vía CR2), NASA MODIS (NDVI), SRTM (relieve) y OpenStreetMap (caminos y edificaciones).

## Uso

Abrir el notebook en Google Colab y ejecutar todo. Los datos se cargan desde este repositorio.
Para redactar el boletín con IA generativa se necesita una clave de Gemini guardada en los Secrets de Colab como `GEMINI_API_KEY`.
