# Data dictionary: `vivienda.csv`

Housing Price Index (IPV, base 2015), **new housing in Catalonia**, as published by the Spanish National Statistics Institute (INE). One row per quarter, most recent first. Index values use 2015 = 100: the four quarters of 2015 average exactly 100 in this file.

| Column | Description | Example |
|---|---|---|
| `Total Nacional` | Geographic level marker | `Nacional` |
| `Comunidades y Ciudades Autónomas` | Region (INE code + name) | `09 Cataluña` |
| `General, vivienda nueva y de segunda mano` | Housing segment | `Vivienda nueva` |
| `Índices y tasas` | Measure type | `Índice` |
| `Periodo` | Quarter (`YYYYTQ`) | `2024T4` |
| `Total` | Index value, base 2015 = 100 (decimal comma) | `199,354` |

**Format:** semicolon-separated, decimal comma, ISO-8859-1 (Latin-1) encoding. Read in R with `read.csv2(..., fileEncoding = "ISO-8859-1")`.

**Coverage:** 2007Q1 to 2024Q4 (72 observations).

## Source & updates

- Table: [INE 25171, IPV: índices por comunidades y ciudades autónomas](https://www.ine.es/jaxiT3/Tabla.htm?t=25171)
- Direct CSV download: <https://www.ine.es/jaxiT3/files/t/es/csv_bdsc/25171.csv>
- The full INE export is also quarterly (the IPV is only published quarterly), but it is much larger because it combines 20 regions, three housing segments (general, new, second-hand) and four measures (the index plus annual, quarterly and year-to-date variation rates). To reproduce this file, filter: *Cataluña* · *Vivienda nueva* · *Índice*.
- Methodology: deed-based index from the General Council of Notaries; new-build prices exclude VAT.
- About the base year: the IPV was originally published in base 2007, but table 25171 is the rebased **2015** series. That is why the four quarters of 2015 average exactly 100 here, while the series itself simply starts in 2007Q1 (with values around 141-150, reflecting pre-crisis prices well above the 2015 level).
