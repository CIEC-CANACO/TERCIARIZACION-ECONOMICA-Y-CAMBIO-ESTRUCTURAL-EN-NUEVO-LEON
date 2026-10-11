# Terciarización económica y cambio estructural en Nuevo León

## Descripción

Este repositorio contiene los materiales de reproducibilidad de un estudio sobre la transformación de la estructura económica de Nuevo León, México, durante el periodo 1980–2024.

La investigación analiza la evolución sectorial del producto interno bruto (PIB), las diferencias interestatales y regionales, los cambios estructurales y los factores asociados con la participación del sector terciario mediante modelos autorregresivos de rezagos distribuidos (ARDL).

## Organización del repositorio

- **01_bases_de_trabajo:** base de datos utilizada en la investigación.
- **02_codigo_R:** código de análisis estadístico y econométrico desarrollado en R.
- **03_figuras:** figuras utilizadas en el manuscrito.
- **04_resultados:** documento HTML con los análisis y resultados.
- **05_documentacion:** diccionario de variables y documentación complementaria.

## Reproducción de resultados

Los análisis se desarrollaron en R y RStudio. Para reproducirlos, descargue el repositorio completo y ejecute el código desde su entorno local, asegurándose de que las rutas de los archivos correspondan con la organización del proyecto.

La base analítica principal se encuentra en `01_bases_de_trabajo/01_base_analitica_terciarizacion.xlsx`.

El archivo HTML permite consultar los procedimientos, las estimaciones y las visualizaciones sin necesidad de ejecutar nuevamente el código.

## Fuentes y tratamiento de los datos

Las fuentes estadísticas incluyen INEGI, CONAPO, SEMARNAT, Data Nuevo León, Banco de México y FRED.

Las variables se construyeron conforme a las definiciones descritas en el manuscrito. Algunas observaciones de escolaridad y población urbana se completaron mediante interpolación y extrapolación lineal.

## Evaluación académica

Los materiales se comparten para facilitar la verificación y reproducción de los resultados durante el proceso de evaluación por pares. Esta versión omite información de autoría y afiliación institucional para preservar el anonimato.
