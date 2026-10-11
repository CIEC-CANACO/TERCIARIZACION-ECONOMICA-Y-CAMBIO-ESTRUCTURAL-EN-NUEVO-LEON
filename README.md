# Terciarización económica y cambio estructural en Nuevo León

## Material de investigación y replicación

Este repositorio reúne las bases de datos, el código en R, las salidas estadísticas y el material complementario de la investigación sobre la terciarización económica de Nuevo León entre 1980 y 2024.

Comprende los análisis desarrollados para el documento de trabajo y la preparación del artículo, incluidos ejercicios exploratorios y resultados complementarios que no necesariamente aparecen en el manuscrito final. Su propósito es documentar la construcción de las variables y facilitar la revisión y reproducción del análisis.

## Organización del repositorio

El archivo `README.md` se encuentra en la raíz del repositorio. Los demás materiales se distribuyen en cuatro carpetas.

### 01_bases_de_trabajo

Contiene las bases y la documentación utilizadas en los análisis sectorial, econométrico, interestatal y regional.

- **`01_base_analitica_terciarizacion.xlsx`**: base principal del análisis descriptivo y econométrico de Nuevo León.
- **`02_construccion_variables_NL.xlsx`**: documentación de la construcción y el tratamiento de las variables estatales.
- **`03_series_tiempo_sectoriales_comparativas.xlsx`**: series sectoriales e información auxiliar para los ejercicios descriptivos y comparativos.
- **`04_base_comparativa_estados.xlsx`**: información para el análisis de las 32 entidades federativas y los agregados regionales durante 1980–2024.
- **`05_fuentes_y_diccionario_variables.xlsx`**: definiciones, fuentes, enlaces de consulta, periodos, unidades de medida y tratamientos de las variables.

El archivo `04_base_comparativa_estados.xlsx` contiene las hojas:

| Hoja | Contenido |
| --- | --- |
| Base | Series anuales de las 32 entidades federativas. |
| Nacional | Serie del agregado nacional. |
| Norte | Información de las entidades de la región Norte. |
| Centro norte | Información de las entidades de la región Centro norte. |
| Centro | Información de las entidades de la región Centro. |
| Sur | Información de las entidades de la región Sur. |

Las hojas `Base` y `Nacional` incluyen las variables `estado`, `año`, `primarias_nivel`, `secundarias_nivel`, `terciarias_nivel` y `pib_nivel`.

### 02_codigo_R

Contiene los scripts de procesamiento, estimación y elaboración de resultados.

**`01_analisis_econometrico_NL.R`**

Incluye el análisis exploratorio, el diagnóstico de multicolinealidad, las pruebas de estacionariedad y cambio estructural, la estimación de modelos ARDL, las pruebas de cointegración y los diagnósticos de residuos y estabilidad.

**`02_codigo_comparativo_y_regionalizacion.R`**

Incluye las participaciones sectoriales estatales y regionales, los cambios entre 1980 y 2024, las comparaciones territoriales de Nuevo León, su contribución al PIB terciario nacional y los indicadores de transformación sectorial. También desarrolla ejercicios complementarios sobre participación inicial, reorientación terciaria y crecimiento real, además de generar mapas y gráficas.

### 03_salidas_R

Contiene las salidas del análisis, entre ellas:

- Documentos HTML del análisis econométrico de Nuevo León.
- `02_codigo_comparativo_y_regionalizacion.html`, con los resultados del análisis interestatal y regional.
- La carpeta `gráficas`, con las visualizaciones exportadas por `02_codigo_comparativo_y_regionalizacion.R`.

Estas salidas permiten consultar resultados sin ejecutar nuevamente los scripts. Los archivos HTML pueden descargarse y abrirse en un navegador.

### 04_material_entrevista

Contiene la guía, la transcripción y el material complementario de la entrevista semiestructurada realizada al Dr. Mario Cerutti, utilizada como apoyo para la interpretación histórica de la transformación productiva de Nuevo León.

## Fuentes y construcción de variables

La información procede del Instituto Nacional de Estadística y Geografía (INEGI), el Consejo Nacional de Población (CONAPO), la Secretaría de Medio Ambiente y Recursos Naturales (SEMARNAT), Data Nuevo León, Banco de México y Federal Reserve Economic Data (FRED). Las referencias y los enlaces específicos se documentan en `05_fuentes_y_diccionario_variables.xlsx`.

La base principal abarca 1980–2024. La inversión extranjera directa (IED) está disponible desde 1999 y las exportaciones desde 2007. Las series de escolaridad y población urbana se completaron mediante interpolación y extrapolación lineal.

La IED se expresa en millones de dólares a precios de 2017. Para su deflactación se utilizó la serie *Gross domestic product (implicit price deflator)*, código `A191RD3A086NBEA`, disponible en FRED.

Las exportaciones, originalmente expresadas en miles de dólares, se convirtieron a pesos mediante el tipo de cambio promedio anual. Posteriormente se expresaron en millones de pesos y se dividieron entre el PIB estatal nominal del mismo año. El indicador resultante es una proporción entre cero y uno.

Los logaritmos naturales del ingreso per cápita y de la IED se calcularon en R.

## Criterios del análisis comparativo

Las participaciones sectoriales corresponden al cociente entre el PIB de cada sector y el PIB total de la entidad. Sus cambios entre 1980 y 2024 se expresan en puntos porcentuales.

La regionalización sigue la clasificación de Banco de México: Norte, Centro norte, Centro y Sur. Las participaciones regionales se calculan dividiendo la suma del PIB sectorial entre la suma del PIB total de las entidades correspondientes; por tanto, están ponderadas por el tamaño económico estatal.

Nuevo León se compara con la región Norte sin la propia entidad y con el agregado nacional. Este último utiliza la serie de la hoja `Nacional` de `04_base_comparativa_estados.xlsx`. El agregado nacional sin Ciudad de México constituye un ejercicio de sensibilidad; Ciudad de México permanece incluida en la comparación principal y en el análisis de las 32 entidades.

Los indicadores complementarios comprenden:

- **Contribución al PIB terciario nacional:** PIB terciario de Nuevo León dividido entre el PIB terciario nacional, expresado en porcentaje.
- **Reorientación terciaria:** cambio de la participación terciaria menos cambio de la participación secundaria, en puntos porcentuales.
- **Crecimiento real anual compuesto:** tasa calculada entre los valores sectoriales de 1980 y 2024.
- **Participación inicial y cambio posterior:** regresión transversal de carácter descriptivo, sin interpretación causal.

## Consulta y reproducción

1. Revisar `05_fuentes_y_diccionario_variables.xlsx` para conocer las definiciones, unidades y tratamientos.
2. Consultar las bases correspondientes al análisis de interés.
3. Revisar las instrucciones de carga de datos y los paquetes utilizados en cada script.
4. Ejecutar el script econométrico o comparativo, según corresponda.
5. Contrastar los resultados con las salidas de `03_salidas_R`.

El repositorio conserva un alcance más amplio que el artículo: la presencia de una estimación o gráfica no implica que forme parte de sus resultados principales. Los ejercicios adicionales documentan el desarrollo de la investigación y deben interpretarse considerando su especificación, cobertura temporal y limitaciones.

Última actualización:
10 de octubre de 2026

## Responsable del repositorio

Francisco Reyna  
CANACO SERVYTUR Monterrey
