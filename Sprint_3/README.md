# Sprint 3: Análisis de Hábitos de Escucha Musical — Springfield y Shelbyville

## 📋 Descripción del Proyecto
Este proyecto forma parte del programa de Análisis de Datos y se centra en el preprocesamiento, limpieza y análisis exploratorio de datos (EDA) para una plataforma de música en streaming. 

El objetivo principal es comparar la actividad de los usuarios y las usuarias en dos ciudades (Springfield y Shelbyville) y evaluar cómo varía el consumo musical según el día de la semana y la hora del día.

---

## 🎯 Objetivos y Preguntas de Investigación
El análisis busca probar tres hipótesis clave:
1. **Actividad por ciudad:** La actividad de escucha de los usuarios difiere entre Springfield y Shelbyville según el día de la semana.
2. **Preferencias por horario (Mañanas y Tardes):** Los lunes por la mañana y los viernes por la tarde, los residentes de cada ciudad escuchan géneros diferentes.
3. **Variación de géneros por ciudad:** Los oyentes de Springfield prefieren géneros diferentes a los de Shelbyville (por ejemplo, mayor preferencia por el pop vs. rock/rap).

---

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python
* **Librerías principales:** 
  * `pandas` (Manipulación, limpieza y filtrado de DataFrames)
* **Entorno:** Jupyter Notebook / Anaconda

---

## 📊 Diccionario de Datos
El dataset principal se encuentra en `/datasets/music_project_en.csv` e incluye la siguiente información:

| Columna | Descripción |
| :--- | :--- |
| `userID` | Identificador único de cada usuario o usuaria |
| `Track` | Título de la canción |
| `artist` | Nombre del artista |
| `genre` | Género musical |
| `City` | Ciudad del usuario (`Springfield` o `Shelbyville`) |
| `time` | Hora del día en la que se reprodujo la pista (`HH:MM:SS`) |
| `Day` | Día de la semana en el que se escuchó la pista |

---

## 🚀 Estructura del Proyecto

### Etapa 1: Descripción de los Datos
* Importación de la librería `pandas`.
* Carga del archivo CSV y lectura de los primeros 10 registros.
* Inspección general con `.info()`, `.shape` y búsqueda de valores nulos o inconsistencias en los datos.

### Etapa 2: Preprocesamiento de Datos
* **Estilo de nombres de columnas:** Corrección de formatos (conversión a *snake_case*, ej. `userID` $\rightarrow$ `user_id`, `Track` $\rightarrow$ `track`, `City` $\rightarrow$ `city`).
* **Valores ausentes (`NaN`):** Identificación e imputación de valores faltantes en columnas como `track`, `artist` y `genre` (reemplazándolos con `'unknown'`).
* **Duplicados:**
  * Eliminación de duplicados explícitos con `.drop_duplicates()`.
  * Identificación y corrección de duplicados implícitos en la columna `genre` (ej. normalización de variantes como `hip`, `hop`, `hip-hop` a un solo género).

### Etapa 3: Prueba de Hipótesis y Análisis
* **Prueba Hipótesis 1:** Filtrado por día (`Monday`, `Wednesday`, `Friday`) y agrupación (`groupby`) por ciudad para evaluar el volumen total de reproducciones.
* **Prueba Hipótesis 2:** Creación de una función para filtrar datos por día y rango horario especifico (ej. mañanas de lunes y tardes de viernes) comparando los Top 10 géneros más escuchados por ciudad.
* **Prueba Hipótesis 3:** Análisis comparativo de la frecuencia general de géneros entre los habitantes de ambas ciudades.

---

## 📝 Conclusiones Principales
*(Agrega aquí un resumen breve de los hallazgos finales tras completar el notebook)*
* **Hipótesis 1:** *[Aceptada / Rechazada]* — Explicación de los resultados por día y ciudad.
* **Hipótesis 2:** *[Aceptada / Rechazada]* — Observaciones sobre géneros en horarios pico.
* **Hipótesis 3:** *[Aceptada / Rechazada]* — Comparación del perfil musical entre Springfield y Shelbyville.