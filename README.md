# MercadoLibre-Funnel-Analysis-SQL

## 🧩 Descripción
Proyecto de análisis de datos realizado con **SQL**, enfocado en entender el comportamiento de los usuarios dentro del embudo de conversión de MercadoLibre y evaluar su **retención a lo largo del tiempo**.

El análisis permite identificar **puntos de fuga**, medir **tasas de conversión por etapa**, analizar **retención por cohortes** y proponer **acciones concretas de mejora** basadas en datos.

---

## 🎯 Objetivo
Responder a las siguientes preguntas de negocio:

- ¿En qué etapa del embudo se pierden más usuarios?
- ¿Cuál es la tasa de conversión entre cada paso del proceso?
- ¿Cómo varía la conversión por país, dispositivo y fuente de tráfico?
- ¿Qué tan bien retenemos a los usuarios después del registro (D7, D14, D21, D28)?
- ¿Qué acciones se pueden tomar para mejorar conversión y retención?

---

## 🛠️ Tecnologías utilizadas
- **SQL**
- **CTEs (Common Table Expressions)**
- Agregaciones y funciones condicionales
- Validaciones de calidad de datos
- Análisis de cohortes
- Metodología **C → F → I (Contexto, Hallazgo, Implicación)**

---

## 🗂️ Dataset del proyecto

### Tablas utilizadas

**mercadolibre_funnel**
- Eventos de usuario a lo largo del proceso de compra.
- Incluye información de país, dispositivo, plataforma y fuente de tráfico.

**mercadolibre_retention**
- Actividad recurrente por usuario.
- Permite analizar retención por cohortes (D1, D7, D14, D21, D28).

---

## 🔄 Metodología

1. Exploración inicial de las tablas y validación de datos.
2. Construcción del **embudo de conversión completo** usando SQL y CTEs.
3. Cálculo de **tasas de conversión** entre etapas.
4. Segmentación del embudo por **país, dispositivo y fuente de tráfico**.
5. Análisis de **retención por cohortes** (D7, D14, D21, D28).
6. Identificación de oportunidades de mejora.
7. Comunicación de resultados mediante un **informe ejecutivo (C → F → I)**.

---

## 📈 Resultados principales

### 🔹 Embudo de conversión
- La mayor caída de usuarios se observa entre **select_item → add_to_cart**, indicando fricción en la decisión de compra.
- Existe una pérdida relevante en **add_payment_info → purchase**, sugiriendo posibles problemas en la etapa de pago.
- La tasa de conversión final varía significativamente por país.

### 🔹 Retención de usuarios
- Las cohortes con mejor retención D28 corresponden a usuarios **mobile** y tráfico **orgánico**.
- Países con baja conversión inicial tienden a mostrar también **peor retención en el tiempo**.
- La retención cae de forma considerable después de D14, lo que indica oportunidades de mejora en la experiencia post-registro.

---

## 🧠 Informe Ejecutivo (C → F → I)

### Contexto
Se analizó el embudo de conversión y la retención de usuarios de MercadoLibre entre enero y agosto de 2025 para identificar pérdidas críticas y oportunidades de crecimiento.

### Hallazgos
- Puntos críticos de fuga en etapas tempranas del embudo.
- Diferencias relevantes de conversión por país y dispositivo.
- Retención decreciente después de la segunda semana post-registro.

### Implicaciones
- Optimizar fichas de producto y mensajes de valor para mejorar el paso a carrito.
- Reducir fricción en pagos (métodos guardados, mensajes de confianza).
- Implementar acciones de retención temprana (onboarding, notificaciones, incentivos).
- Priorizar inversión en canales con mayor retención a largo plazo.

## 📂 Estructura del repositorio
  MercadoLibre-Funnel-Retention-Analysis/

├── README.md

  ├── sql/

     ├── 01_data_exploration.sql
     
     ├── 02_funnel_analysis.sql

     ├── 03_funnel_by_country.sql

     ├── 04_retention_analysis.sql
 
     └── 05_cohort_analysis.sql

  ├── results/

    └── executive_report_CFI.xlsx

    └── funnel_metrics.csv

    └── retention_cohorts.csv   


---

## ▶️ Cómo ejecutar el proyecto

1. Cargar las tablas `mercadolibre_funnel` y `mercadolibre_retention` en tu motor SQL.
2. Ejecutar los scripts ubicados en la carpeta `/sql`.
3. Revisar los resultados agregados para análisis del embudo y retención.
4. Interpretar los hallazgos siguiendo el informe ejecutivo.


