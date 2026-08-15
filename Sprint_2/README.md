# 🛒 Limpieza y Procesamiento Avanzado de Clientes — Store 1

## 📌 Descripción del Proyecto

Como continuación directa del Programa de Fidelización de Clientes, Store 1 ha establecido requisitos analíticos más complejos para profundizar en el comportamiento de sus usuarios. Este proyecto aborda el procesamiento y la normalización de una base de datos cruda de clientes mediante el uso de estructuras de datos, condicionales y funciones en Python.

El objetivo final es transformar estos datos para responder preguntas clave de negocio, calcular los ingresos globales, identificar segmentos de clientes jóvenes de alto valor y automatizar la extracción de perfiles para campañas de marketing dirigidas.

---

## 🛠️ Objetivos Principales

* **Normalización de Registros:** Limpiar espacios y caracteres especiales en nombres, separar nombre y apellido, convertir edades a enteros y homogeneizar categorías a minúsculas.
* **Métricas Globales:** Calcular los ingresos totales acumulados a partir de los registros de gasto por usuario.
* **Segmentación Estratégica:** Filtrar clientes de alto interés comercial (usuarios menores de 30 años con compras superiores a $1,000 USD).
* **Análisis por Categoría:** Identificar patrones de compra específicos en categorías clave (como *"clothes"* o *"home"*).
* **Automatización:** Implementar funciones reutilizables que permitan filtrar y extraer la información de los clientes según la categoría consultada.

---

## 📊 Estructura de Datos

Los registros procesados finales estructuran la información en listas nativas bajo el siguiente formato:
* **user_id:** Identificador único del cliente.
* **user_name:** Sublista con el nombre y apellido procesados `[nombre, apellido]`.
* **user_age:** Edad del usuario como número entero (`int`).
* **fav_categories_low:** Lista de categorías favoritas transformadas a minúsculas.
* **total_spendings:** Lista con los montos gastados por categoría.

---

## 🔧 Herramientas Utilizadas

* **Lenguaje:** Python (Estructuras de datos anidadas, métodos de cadenas, bucles `for`, lógica condicional `if/and/in` y funciones personalizadas).