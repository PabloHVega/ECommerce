# Análisis de Clientes

_Generado el 13/06/2026 · Fecha de referencia: 29/02/2020_

## 1. Distribución del Gasto por Cliente

|       |    gasto |
|:------|---------:|
| count | 11040    |
| mean  |    56.3  |
| std   |    81.73 |
| min   |     0.13 |
| 25%   |    16.22 |
| 50%   |    32.74 |
| 75%   |    60.3  |
| 90%   |   121.28 |
| 95%   |   188.89 |
| 99%   |   393.95 |
| max   |  1559.21 |


## 2. Concentración del Ingreso (Pareto)

- Top **1%** de clientes (110) → **10.6%** del ingreso total (€65,594.93)
- Top **5%** de clientes (552) → **29.1%** del ingreso total (€181,143.54)
- Top **10%** de clientes (1,104) → **42.4%** del ingreso total (€263,768.62)
- Top **20%** de clientes (2,208) → **58.9%** del ingreso total (€366,296.18)


## 3. Compradores Únicos vs Recurrentes

| Segmento | Clientes | % del Total |
|---|---|---|
| One-shot (1 compra) | 8,697 | 78.8% |
| Recurrentes (>1 compra) | 2,343 | 21.2% |
| **Total** | **11,040** | **100%** |


## 4. Distribución del Número de Compras por Cliente (top 10 valores)

|   Nº Compras |   Clientes |   % del Total |
|-------------:|-----------:|--------------:|
|            1 |       8697 |          78.8 |
|            2 |       1420 |          12.9 |
|            3 |        469 |           4.2 |
|            4 |        204 |           1.8 |
|            5 |         96 |           0.9 |
|            6 |         67 |           0.6 |
|            7 |         25 |           0.2 |
|            8 |         20 |           0.2 |
|            9 |         20 |           0.2 |
|           10 |          5 |           0   |


## 5. Top 20 Clientes por Gasto Total

|   usuario |   compras |   productos |   precio_medio |   gasto | fecha_ultima   |   % s/ total |
|----------:|----------:|------------:|---------------:|--------:|:---------------|-------------:|
| 573823111 |         2 |         268 |           5.82 | 1559.21 | 2020-02-21     |         0.25 |
| 539751397 |        13 |         236 |           6.16 | 1453.37 | 2020-02-19     |         0.23 |
| 556579890 |         4 |         506 |           2.75 | 1392.45 | 2020-02-27     |         0.22 |
| 442763940 |         8 |         195 |           6.37 | 1241.53 | 2019-12-23     |         0.2  |
| 561592095 |         3 |          94 |          11.81 | 1109.7  | 2019-10-31     |         0.18 |
| 527739278 |        13 |         244 |           4.39 | 1071    | 2020-02-16     |         0.17 |
| 527806771 |        13 |         195 |           4.86 |  948.01 | 2020-02-20     |         0.15 |
| 430220205 |         6 |         190 |           4.99 |  947.3  | 2020-02-29     |         0.15 |
| 491009486 |         1 |         219 |           4.32 |  946.2  | 2020-02-12     |         0.15 |
| 520501669 |        11 |          64 |          14.27 |  913.01 | 2020-01-17     |         0.15 |
| 492650335 |        18 |         243 |           3.72 |  904.53 | 2020-02-25     |         0.15 |
| 564398840 |         4 |          80 |          11.12 |  889.48 | 2020-01-06     |         0.14 |
| 596723316 |         6 |         137 |           6.45 |  884.16 | 2020-01-31     |         0.14 |
| 458913731 |         4 |          92 |           9.54 |  877.93 | 2020-02-28     |         0.14 |
| 233280499 |        11 |         200 |           4.29 |  858.26 | 2020-02-27     |         0.14 |
| 570593977 |         1 |         181 |           4.68 |  847.12 | 2020-01-22     |         0.14 |
| 564321657 |        23 |         122 |           6.72 |  820.04 | 2020-02-27     |         0.13 |
| 414659837 |         9 |         235 |           3.37 |  791.02 | 2020-02-21     |         0.13 |
| 234651934 |         1 |         143 |           5.34 |  763.81 | 2020-02-25     |         0.12 |
| 399445659 |         3 |         113 |           6.73 |  760.03 | 2020-02-10     |         0.12 |


## 6. Análisis RFM (Recencia · Frecuencia · Monetario)

| segmento    |   clientes |   gasto_medio |   gasto_total |   recencia_media |   compras_medias |   % clientes |   % ingreso |
|:------------|-----------:|--------------:|--------------:|-----------------:|-----------------:|-------------:|------------:|
| Champions   |       1798 |        147.83 |     265803    |            25.6  |             2.84 |         16.3 |        42.8 |
| En riesgo   |       1885 |         22.44 |      42294.5  |           109.02 |             1    |         17.1 |         6.8 |
| Leales      |       2904 |         56.07 |     162829    |            46.32 |             1.34 |         26.3 |        26.2 |
| Perdidos    |        701 |         11.88 |       8324.73 |           126.94 |             1    |          6.3 |         1.3 |
| Potenciales |       3752 |         37.93 |     142298    |            75.94 |             1.03 |         34   |        22.9 |


## 7. Correlaciones entre Variables de Cliente

|                      |   compras |   productos |   precio_medio |   gasto |   productos_por_compra |
|:---------------------|----------:|------------:|---------------:|--------:|-----------------------:|
| compras              |     1     |       0.622 |         -0.068 |   0.611 |                  0.062 |
| productos            |     0.622 |       1     |         -0.161 |   0.836 |                  0.694 |
| precio_medio         |    -0.068 |      -0.161 |          1     |   0.115 |                 -0.198 |
| gasto                |     0.611 |       0.836 |          0.115 |   1     |                  0.528 |
| productos_por_compra |     0.062 |       0.694 |         -0.198 |   0.528 |                  1     |


## 8. Clientes Dormidos por Tramo de Recencia

| Tramo recencia   |   Clientes |    % |
|:-----------------|-----------:|-----:|
| 0-30 días        |       2714 | 24.6 |
| 31-60 días       |       2264 | 20.5 |
| 61-90 días       |       1976 | 17.9 |
| 91-180 días      |       4007 | 36.3 |


## 9. Segmentación Cruzada: Gasto vs Frecuencia de Compra

_(medianas usadas como corte: gasto=32.74€, compras=1)_

| cuadrante                    |   clientes |   gasto_medio |   gasto_total |   % clientes |   % ingreso |
|:-----------------------------|-----------:|--------------:|--------------:|-------------:|------------:|
| Alto gasto · Alta frecuencia |       5522 |         95.3  |      526234   |           50 |        84.7 |
| Bajo gasto · Alta frecuencia |       5518 |         17.27 |       95315.3 |           50 |        15.3 |


## 10. Detección de Outliers

| Tipo de Outlier | Umbral | Nº Clientes |
|---|---|---|
| Gasto extremadamente alto (>p99) | €393.95 | 111 |
| Productos/compra extremadamente alto (>p99) | 42.0 uds | 107 |
| Precio medio extremadamente bajo (<p1) | €1.17 | 111 |
