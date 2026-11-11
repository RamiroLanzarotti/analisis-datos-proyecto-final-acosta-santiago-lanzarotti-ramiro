# Ventas de lácteos 2024: un negocio sin dependencias

**Autores:** Santiago Acosta y Ramiro Lanzarotti

**Curso:** Herramientas básicas para el análisis de datos

---

## Objetivo

Comprender qué variables explican la facturación de un distribuidor mayorista de lácteos en Estados Unidos durante 2024, a partir de tres preguntas:

1. ¿Qué factores generaron los mejores resultados de facturación a lo largo del año?
2. ¿Qué diferencias hay entre el comportamiento de las ciudades y estados?
3. ¿La fortaleza de los supermercados varía por estado, o hay un dominante?

## Dataset

[Dataset ventas lácteos 2024](https://www.kaggle.com/datasets/hectorconde/dataset-ventas-lacteos-2024) (Kaggle): 10.000 órdenes de venta con fecha, vendedor, supermercado, estado, ciudad, categoría, producto, precio, cantidad, valor total y forma de pago.

Copia local: [`data/raw/dataset_ventas_lacteos_2024.csv`](data/raw/dataset_ventas_lacteos_2024.csv)

## Pasos realizados

1. **Exploración y limpieza en Python** ([ver notebook](https://nbviewer.org/github/RamiroLanzarotti/analisis-datos-proyecto-final-acosta-santiago-lanzarotti-ramiro/blob/main/notebooks/analisis-de-ventas-lacteos-2024.ipynb)): revisión de tipos, nulos y duplicados, conversión de fechas y renombrado de columnas con Pandas.
2. **Análisis** de ventas y facturación por estado, ciudad, mes, vendedor, categoría y producto, con gráficos en Matplotlib.
3. **Dashboard en Power BI** ([archivo .pbix](dashboard/analisis-ventas-lacteos-2024.pbix)): ajuste del separador decimal en Power Query, medidas DAX y dos páginas de visualización.

![Geografía y clientes](dashboard/Geograf%C3%ADa%20y%20clientes.png)

![Quesos vs. Mantequilla](dashboard/Quesos%20vs%20Mantequilla.png)

## Hallazgos

- **Facturación:** más órdenes no implica más ingresos. Quesos y Mantequilla suman el 49% de la facturación y explican los altibajos: Quesos lidera 7 de 12 meses y Mantequilla domina el último trimestre.
- **Ciudades:** las diferencias son pequeñas. Tampa y Miami se apartan del patrón según cómo vendieron Quesos y Mantequilla.
- **Supermercados:** no hay un dominante. Ningún cliente supera el 6% del total y cada estado tiene un líder distinto.

**Limitación:** las distribuciones son muy uniformes, lo que sugiere un dataset sintético; las conclusiones aplican a estos datos.

## Fuentes

- hectorconde (s.f.). *Dataset ventas lácteos 2024* [Dataset]. Kaggle. https://www.kaggle.com/datasets/hectorconde/dataset-ventas-lacteos-2024
- Documentación de Pandas: https://pandas.pydata.org/docs/
- Documentación de Matplotlib: https://matplotlib.org/stable/
- Documentación de Power BI: https://learn.microsoft.com/es-es/power-bi/
- Imágenes: capturas propias del dashboard en Power BI.
