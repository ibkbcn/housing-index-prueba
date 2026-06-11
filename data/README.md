# Data dictionary: `mercamadrid.xlsx`

Processed dataset behind the analysis and the Power BI dashboard. One row per product variety, origin and month, January to September 2024 (27,571 rows x 16 columns). It is the output of [`notebooks/01_cleaning_transformation.ipynb`](../notebooks/01_cleaning_transformation.ipynb).

| Column | Description |
|---|---|
| `fecha_desde`, `fecha_hasta` | Start and end date of the reporting month |
| `código_variedad`, `descripción_variedad` | Product variety code and name |
| `origen`, `descripción_origen` | Origin code and name (Spanish province or foreign country) |
| `kilos` | Volume traded in the period (kg) |
| `precio_más_frecuente`, `precio_máximo`, `precio_mínimo` | Most frequent, maximum and minimum price (EUR/kg) |
| `var_precios` | Price variation |
| `trimestre` | Quarter (1 to 3) |
| `tipo_general`, `nueva_categoria` | Product groupings created during transformation |
| `categoria_general` | General typology: Vegetales, Carne, Pescado, Otros |
| `nacional_inter` | Origin flag: ESPAÑA (domestic) vs RESTO (imported) |

**Source:** [Mercamadrid: volumen y precio, Madrid City Council open data portal](https://data.europa.eu/data/datasets/https-datosmadrid-es-egob-catalogo-300357-0-mercamadrid-volumen-precio) (raw file `volpre2024.csv`). Prices and volumes as published by Mercamadrid; origin coordinates and distances to Madrid are computed in notebook 02.
