# Data dictionary — `vivienda.csv`

Housing Price Index (IPV, base 2015), **new housing in Catalonia**, as published by the Spanish National Statistics Institute (INE). One row per quarter, most recent first.

| Column | Description | Example |
|---|---|---|
| `Total Nacional` | Geographic level marker | `Nacional` |
| `Comunidades y Ciudades Autónomas` | Region (INE code + name) | `09 Cataluña` |
| `General, vivienda nueva y de segunda mano` | Housing segment | `Vivienda nueva` |
| `Índices y tasas` | Measure type | `Índice` |
| `Periodo` | Quarter (`YYYYTQ`) | `2024T4` |
| `Total` | Index value, base 2015 = 100 (decimal comma) | `199,354` |

**Format:** semicolon-separated, decimal comma, ISO-8859-1 (Latin-1) encoding — read in R with `read.csv2(..., fileEncoding = "ISO-8859-1")`.

**Coverage:** 2007Q1 – 2024Q4 (72 observations).

## Source & updates

- Table: [INE 25171 — IPV. Índices por comunidades y ciudades autónomas](https://www.ine.es/jaxiT3/Tabla.htm?t=25171)
- Direct CSV download: <https://www.ine.es/jaxiT3/files/t/es/csv_bdsc/25171.csv> (then filter: *Cataluña* · *Vivienda nueva* · *Índice*)
- Methodology: deed-based index from the General Council of Notaries; new-build prices exclude VAT.
