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

1. Abrir el notebook en Google Colab.
2. Activar la GPU: **Entorno de ejecución → Cambiar tipo de entorno → T4 GPU → Guardar** (en inglés: **Runtime → Change runtime type → T4 GPU → Save**).
3. **Entorno de ejecución → Ejecutar todo** (**Runtime → Run all**).
4. Al final, el notebook pide el correo de destino del boletín. Si se deja vacío, el boletín solo se guarda como HTML.

El boletín se redacta con Qwen2.5, un modelo de IA generativa de código abierto que corre en Colab sin clave.
Para enviar el correo se usa una cuenta de Gmail con contraseña de aplicación (ver sección 7.1 del notebook).
