# US Accidents — Análisis de Accidentes Graves con Power BI

## Descripción del proyecto

Este proyecto analiza un conjunto de datos de accidentes de tránsito con el objetivo de identificar patrones relacionados con la **severidad de los accidentes**, con especial atención en los accidentes graves.

El análisis se organiza en cuatro dimensiones principales:

* **Temporal:** cuándo ocurren los accidentes.
* **Clima:** bajo qué condiciones meteorológicas ocurren.
* **Geográfica:** dónde se concentran dentro de USA.
* **Infraestructura:** qué características de la infraestructura vial están presentes.

El dashboard fue diseñado para combinar una vista ejecutiva con hojas exploratorias que permiten analizar los accidentes desde diferentes perspectivas y cambiar el análisis mediante filtros, especialmente por **nivel de severidad**.

---

# Dashboard

## 1. Resumen Ejecutivo

La página de resumen ejecutivo concentra los principales resultados del análisis en una sola vista.

### Indicadores principales

* **Accidentes totales**
* **Accidentes graves**
* **Porcentaje de accidentes graves**

Estos indicadores proporcionan una visión general del volumen de accidentes y del peso que representan los accidentes graves dentro del conjunto analizado.

### Principales hallazgos

**Patrón horario**

Los accidentes en general presentan sus principales concentraciones durante las **7–8 AM y 4–5 PM**. Al analizar únicamente los accidentes **graves**, el patrón cambia: **4–5 PM** se convierte en el periodo principal, seguido por **7–8 AM**.

**Patrón mensual**

El número total de accidentes presenta concentraciones mayores hacia los últimos meses del año y los primeros meses del siguiente periodo. En contraste, los accidentes graves presentan una distribución relativamente estable a lo largo de los meses no un porcentaje del total sino el misma rango de cantidad de accidentes graves.

**Día de la semana**

Los dias entre semana presenta el mayor volumen de accidentes, mientras que los accidentes disminuyen durante el fin de semana. Este comportamiento también se observa al analizar los accidentes graves.

**Clima**

La mayor parte de los accidentes ocurre bajo condiciones meteorológicas normales. Sin embargo, las variables térmicas muestran diferencias según la severidad: la **temperatura promedio y el Wind Chill disminuyen a medida que aumenta la gravedad**.

La humedad presenta un incremento moderado con la severidad, mientras que presión, visibilidad y precipitación presentan diferencias reducidas entre los niveles de gravedad analizados.

**Distribución geográfica**

Los accidentes no están distribuidos uniformemente. Algunos estados, ciudades y counties concentran una cantidad de accidentes significativamente mayor que otros en especial **California** concentrando el **18.97** de los accidentes.

**Infraestructura**

Entre las características de infraestructura registradas, **Traffic Signal** y **Crossing** presentan las mayores proporciones, alrededor del 10% cada una. Station, Stop y Junction aparecen con proporciones menores, mientras que categorías como Roundabout, Turning Loop, Railway, Bump, Give Way, Amenity y Traffic Calming presentan una presencia reducida o nula.

> Los hallazgos descriptivos del dashboard muestran asociaciones y patrones dentro de los datos; no implican por sí mismos relaciones causales.

---

# 2. Análisis Temporal

Esta hoja permite explorar cómo se distribuyen los accidentes a través del tiempo.

### Análisis incluido

* Distribución de accidentes por **hora**
* Distribución por **mes-año**
* Distribución por **día de la semana**
* Comparación entre accidentes totales y accidentes graves

### Principal hallazgo

El comportamiento cambia cuando se pasa del conjunto total de accidentes al subconjunto de accidentes graves.

En el total de accidentes, las horas de **7–8 AM y 4–5 PM** destacan claramente. Para los accidentes graves, el periodo de **4–5 PM** adquiere mayor relevancia, seguido por **7–8 AM**.

La hoja permite utilizar el filtro de severidad para explorar cómo cambia este comportamiento entre los diferentes niveles.

---

# 3. Análisis Climático

La hoja climática está diseñada como una página de **exploración**, permitiendo analizar las variables meteorológicas disponibles y observar cómo cambian al modificar la severidad seleccionada.

### Variables analizadas

* Temperatura
* Wind Chill
* Humedad
* Presión atmosférica
* Visibilidad
* Precipitación
* Condición meteorológica

### Interactividad

El **segmentador de severidad** permite cambiar el subconjunto de accidentes analizado y observar cómo se modifican las medidas y visualizaciones de clima.

### Principal hallazgo

Los accidentes graves presentan valores promedio de temperatura y Wind Chill menores que los accidentes de menor severidad.

Por otro lado, las condiciones meteorológicas normales concentran la mayor cantidad de accidentes en términos absolutos. Esta observación debe interpretarse considerando la frecuencia con la que cada condición aparece en los datos.

La página está orientada principalmente a la exploración, por lo que las diferentes medidas climáticas pueden analizarse de forma interactiva.

---

# 4. Análisis Geográfico

Esta hoja permite explorar la distribución espacial de los accidentes y analizar cómo cambia dependiendo de la severidad seleccionada.

### Niveles geográficos

* Estado
* County
* Ciudad

### Análisis incluido

* Concentración de accidentes por estado
* Principales estados según número de accidentes
* Exploración de counties y ciudades
* Distribución geográfica mediante mapas
* Comparación entre niveles de severidad

### Interactividad

El **segmentador de severidad** permite analizar la distribución geográfica de todos los accidentes o concentrarse en niveles específicos, incluyendo los accidentes graves.

Esto permite identificar si los lugares con mayor volumen de accidentes generales también concentran los accidentes de mayor severidad.

---

# 5. Análisis de Infraestructura

Esta hoja analiza las características de infraestructura vial registradas en los accidentes.

### Características analizadas

Entre otras:

* Traffic Signal
* Crossing
* Station
* Stop
* Junction
* Roundabout
* Turning Loop
* No Exit
* Traffic Calming
* Railway
* Bump
* Give Way
* Amenity

### Principales observaciones

Traffic Signal y Crossing presentan las mayores proporciones dentro de las características registradas, con aproximadamente **10%** cada una.

Station, Stop y Junction aparecen en proporciones menores, alrededor del **5%**, mientras que varias categorías presentan una presencia muy reducida o nula.

Esta página se utiliza principalmente para explorar la presencia de características de infraestructura y su distribución entre los accidentes.

> La frecuencia de una característica no debe interpretarse directamente como evidencia de que dicha infraestructura aumenta la severidad de un accidente. Para establecer una relación de ese tipo sería necesario considerar tasas o denominadores adecuados y realizar un análisis estadístico adicional.

---

# Interactividad del Dashboard

El dashboard utiliza filtros y segmentadores para permitir una exploración dinámica.

El **segmentador de severidad** es uno de los principales mecanismos de interacción y permite analizar cómo cambian los patrones temporales, climáticos y geográficos dependiendo del nivel de gravedad seleccionado.

Las diferentes hojas están diseñadas para responder preguntas complementarias:

| Hoja                  | Pregunta principal                                                                    |
| --------------------- | ------------------------------------------------------------------------------------- |
| **Resumen Ejecutivo** | ¿Cuáles son los principales patrones de los accidentes y accidentes graves?           |
| **Temporal**          | ¿Cuándo ocurren los accidentes y cómo cambia el patrón según la severidad?            |
| **Clima**             | ¿Qué características meteorológicas presentan los accidentes?                         |
| **Geográfico**        | ¿Dónde se concentran los accidentes y cómo cambia la distribución según la severidad? |
| **Infraestructura**   | ¿Qué características de infraestructura aparecen en los accidentes?                   |

---

# Objetivo del análisis

El propósito del proyecto no es únicamente mostrar el número de accidentes, sino utilizar Power BI para identificar **patrones relevantes de severidad**, facilitar la exploración de los datos y transformar un conjunto de datos de gran tamaño en información útil para el análisis.

El dashboard busca demostrar el uso de:

* Modelado y transformación de datos
* Medidas DAX
* Segmentadores y filtros
* Visualización de datos
* Análisis temporal
* Análisis geográfico
* Análisis exploratorio
* Comunicación de hallazgos mediante un resumen ejecutivo
