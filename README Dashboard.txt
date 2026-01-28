📊 Dashboard de Análisis de Ventas y Rentabilidad – Power BI

👤 Autor: Nicolás Barrios
💼 Perfil: Ingeniero Biomédico | Data Analyst / BI Analyst
🛠️ Herramientas: Power BI · Power Query · DAX · Modelado Dimensional (Kimball)

📌 Descripción General

Este proyecto desarrolla una solución integral de Business Intelligence en Power BI para analizar el desempeño comercial, la rentabilidad y la eficiencia operativa a partir de datos transaccionales de ventas.

Se implementó un modelo dimensional basado en Star Schema (metodología Kimball), garantizando:

✔️ Alto rendimiento en consultas
✔️ Escalabilidad del modelo
✔️ Claridad analítica
✔️ Confiabilidad en los KPIs

El dashboard permite monitorear tendencias, identificar oportunidades de crecimiento y respaldar la toma de decisiones basadas en datos.

🎯 Valor para el Negocio:

📈 Identificar productos, regiones y segmentos de mayor y menor desempeño

💰 Analizar tendencias de ingresos, utilidad y margen

🚚 Evaluar eficiencia logística

📊 Monitorear crecimiento interanual

🧭 Apoyar procesos de planeación estratégica y forecasting


📂 Dataset

📍 Fuente: Dataset público de ventas de una multinacional tecnológica.
📍 Granularidad: Línea de orden de venta

Variables principales:

Sales, Profit, Quantity, Discount

Order Date, Ship Date

Customer, Product, Geography, Ship Mode

🧹 Limpieza y Preparación de Datos (ETL)

El proceso ETL se realizó en Power Query e incluyó:

✔️ Normalización de formato regional
✔️ Normalización de texto
✔️ Integridad geográfica
✔️ Eliminación de duplicados
✔️ Generación de surrogate keys mediante índices
✔️ Integración con FactSales mediante procesos de merge

🧩 Arquitectura del Modelo de Datos

Se implementó un esquema en estrella con la siguiente estructura:

📍 Tabla de Hechos 

1) FactSales: Sales, Profit, Quantity, Discount, 
Order Date, Ship Date,CustomerKey, ProductKey, 
GeographyKey, ShipModeKey

📍 Tablas Dimensión

1) DimCustomer: Cliente y Segmento

2) DimProduct: Producto, Categoría y Subcategoría

3) DimGeography: País, Estado, Ciudad, Región

4) DimShipMode: Tipo de Envío

5) DimDate: Construcción dinámica mediante DAX (CALENDAR) basada en rango real de datos.


⚙️ Decisiones de Modelado

- Integración de Categoría y Subcategoría en DimProduct (evitando Snowflake)

- Implementación de surrogate keys en todas las dimensiones

- Definición de granularidad a nivel de línea de venta

- Relaciones 1:* con filtrado unidireccional

📈 Diseño del Dashboard y Navegación

La navegación se gestiona mediante:

🔖 Bookmarks

🔘 Botones interactivos

🔄 Reset de filtros


📊 Secciones Principales del Dashboard

- Overview

- Segmentación

- Análisis Regional

- Análisis de Producto

- Product Insights

- Forecasting

- Actual vs Año Anterior

- Análisis Semanal


🧠 Retos Técnicos y Soluciones

🔹 Formato incorrecto de datos
→ Configuración regional

🔹 Falta de claves geográficas
→ Implementación de surrogate keys

🔹 Diseño jerárquico
→ Integración en dimensiones

🔹 Navegación compleja
→ Uso de Bookmarks

🚀 Habilidades Demostradas

✔️ Modelado Dimensional (Star Schema)
✔️ ETL en Power Query
✔️ Limpieza de Datos
✔️ Análisis Temporal
✔️ Visualización Ejecutiva
✔️ Data Storytelling
✔️ Optimización de Rendimiento