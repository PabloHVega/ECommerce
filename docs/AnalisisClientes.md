# Análisis de Clientes — ECommerce Cosméticos

_Generado el 18/06/2026  ·  Fecha de referencia: 29/02/2020_

---

## Resumen Ejecutivo

El ecommerce cuenta con **11,040 clientes únicos** con al menos una compra, generando un ingreso total acumulado de **€621,549.60** (gasto medio por cliente: **€56.30**).

Las tres palancas estratégicas identificadas son:

1. **Retención de Champions y Leales** — solo el 26.5% de los clientes pero aportan el **56.5% del ingreso total**.
2. **Reactivación** — el 41.9% de clientes (En riesgo + Perdidos) tiene historial de compra y puede ser recuperado con retargeting o email.
3. **Conversión de Potenciales** — el 31.5% de la base (mayor grupo individual) tiene recencia y/o gasto aceptables pero baja frecuencia; son los más convertibles.


---

## 1. Estructura de la Base de Clientes

### 1.1 Distribución del Gasto

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



**Insights:**

- La mediana de gasto es **€32.74** frente a una media de **€56.30** — distribución fuertemente sesgada a la derecha.
- El percentil 90 (€121.28) triplica la mediana: existe un segmento premium reducido pero de alto valor.
- El percentil 99 supera los €394, indicando outliers de ultra-alto valor que merecen tratamiento VIP individual.


### 1.2 Concentración de Ingresos (Ley de Pareto)

- Top **1%** de clientes (110) → **10.6%** del ingreso (€65,594.93)
- Top **5%** de clientes (552) → **29.1%** del ingreso (€181,143.54)
- Top **10%** de clientes (1,104) → **42.4%** del ingreso (€263,768.62)
- Top **20%** de clientes (2,208) → **58.9%** del ingreso (€366,296.18)

> El top 20% de clientes concentra el **58.9%** del ingreso, confirmando (y superando) la ley de Pareto.


### 1.3 Compradores Únicos vs Recurrentes

| Segmento | Clientes | % |
|---|---|---|
| One-shot (1 compra)     | 8,697 | 78.8% |
| Recurrentes (>1 compra) | 2,343 | 21.2% |
| **Total**               | **11,040** | **100%** |


> **78.8% de la base solo ha comprado una vez.** Convertir el 10% en recurrentes incrementaría el LTV medio de forma significativa.


---

## 2. Análisis por Dimensión RFM

_Cada dimensión se puntúa de 1 (peor) a 5 (mejor). Nota: la dimensión F (Frecuencia) solo toma valores 1-2 en esta base de datos porque el 79% de clientes son one-shot._


### 2.1 Recencia (R) — días desde la última compra (5 = más reciente)

|   Nivel |   clientes |   gasto_medio |   % clientes |
|--------:|-----------:|--------------:|-------------:|
|       1 |       2165 |         41.18 |         19.6 |
|       2 |       2202 |         46.98 |         19.9 |
|       3 |       2235 |         49    |         20.2 |
|       4 |       2160 |         59.78 |         19.6 |
|       5 |       2278 |         83.54 |         20.6 |



### 2.2 Frecuencia (F) — número de compras (5 = más compras)

|   Nivel |   clientes |   gasto_medio |   % clientes |
|--------:|-----------:|--------------:|-------------:|
|       1 |      10117 |         44.16 |         91.6 |
|       2 |        923 |        189.36 |          8.4 |



### 2.3 Monetario (M) — gasto total (5 = mayor gasto)

|   Nivel |   clientes |   gasto_medio |   % clientes |
|--------:|-----------:|--------------:|-------------:|
|       1 |       2219 |          9.94 |         20.1 |
|       2 |       2199 |         19.04 |         19.9 |
|       3 |       2206 |         32.98 |         20   |
|       4 |       2209 |         53.7  |         20   |
|       5 |       2207 |        165.94 |         20   |



**Insights:**

- **Recencia (R)**: distribución uniforme entre niveles — la base cubre todo el período analizado sin concentración en ningún tramo temporal.
- **Frecuencia (F)**: F solo tiene 2 valores (1 y 2) porque el 79% de clientes son one-shot. El gasto medio de clientes con F=2 es ~4x mayor que los de F=1: **la segunda compra es el mayor multiplicador de valor disponible**.
- **Monetario (M)**: correlación directa entre nivel M y gasto. M=5 multiplica por ~16x el gasto de M=1. La cola de alto valor es pequeña pero determinante para el negocio.


---

## 3. Análisis Cruzado de Dimensiones RFM


### R × F (Recencia × Frecuencia) — Gasto Medio (€)

|   R |    1 |     2 |
|----:|-----:|------:|
|   5 | 51.1 | 221.6 |
|   4 | 45.9 | 171   |
|   3 | 40.8 | 159.2 |
|   2 | 44.3 | 127.8 |
|   1 | 39.7 | 164.8 |



### R × M (Recencia × Monetario) — Gasto Medio (€)

|   R |    1 |    2 |    3 |    4 |     5 |
|----:|-----:|-----:|-----:|-----:|------:|
|   5 |  9.6 | 19.1 | 33   | 54.1 | 205.2 |
|   4 |  9.8 | 19.1 | 33.2 | 54   | 163   |
|   3 | 10.2 | 19.1 | 32.7 | 54.4 | 148.1 |
|   2 |  9.9 | 19   | 33.2 | 53.3 | 135.6 |
|   1 | 10.1 | 19   | 32.9 | 52.8 | 136.1 |



**Insights:**

- Los clientes con **R=5, F=2** (recientes y con múltiples compras) alcanzan un gasto medio de €222 — son los Champions inequívocos.
- La dimensión R no discrimina el gasto cuando F y M son bajos: todos los clientes one-shot con M=1 gastan ~€10 independientemente de cuándo compraron.
- Los clientes con **R=1-2, M=4-5** (alto gasto histórico pero inactivos) son los de mayor riesgo: han demostrado capacidad de gasto pero llevan mucho tiempo sin volver.
- Los clientes con **R=4-5, F=1, M=3-5** son la oportunidad más inmediata de cross-sell: recientes, buen ticket pero aún no han repetido compra.


---

## 4. Curva de Valor RFM

_(valor_RFM = R + F + M; rango efectivo 3–12 dado que F max = 2)_

|   valor_RFM |   clientes |   pct_clientes |   gasto_medio |   pct_ingreso |
|------------:|-----------:|---------------:|--------------:|--------------:|
|           3 |        486 |           4.4  |       10.1058 |          0.79 |
|           4 |        943 |           8.54 |       14.7105 |          2.23 |
|           5 |       1404 |          12.72 |       20.4463 |          4.62 |
|           6 |       1802 |          16.32 |       29.0395 |          8.42 |
|           7 |       1957 |          17.73 |       42.4524 |         13.37 |
|           8 |       1522 |          13.79 |       57.5248 |         14.09 |
|           9 |       1122 |          10.16 |       70.1533 |         12.66 |
|          10 |        872 |           7.9  |      101.297  |         14.21 |
|          11 |        566 |           5.13 |      161.503  |         14.71 |
|          12 |        366 |           3.32 |      253.128  |         14.91 |



**Insights:**

- El nivel máximo alcanzable es **valor_RFM=12** (no 15) porque la F máxima es 2 en esta base de datos.
- Los clientes con valor_RFM=12 (Champions) representan solo el **3.3%** pero aportan el **14.9%** del ingreso.
- La curva de gasto medio es casi exponencial: valor_RFM=12 → €253 vs valor_RFM=3 → €10 (25x más).
- Solo **16 combinaciones RFM** cubren el 80% del ingreso total (de 45 únicas).


---

## 5. Segmentación RFM Formal — 5 Segmentos

| Segmento | Criterio valor_RFM | Descripción |

|---|---|---|

| Champions   | = 12   | Clientes más valiosos: recientes, frecuentes y de alto gasto |

| Leales      | 9-11  | Buenos clientes con comportamiento consistente |

| Potenciales | 7-8   | Compran ocasionalmente con gasto aceptable |

| En riesgo   | 5-6   | Compraron en el pasado pero llevan tiempo inactivos |

| Perdidos    | <= 4  | Baja puntuación en todas las dimensiones |



| segmento_rfm   |   clientes |   gasto_medio |   gasto_total |   recencia_media |   compras_medias |   pct_clientes |   pct_ingreso |
|:---------------|-----------:|--------------:|--------------:|-----------------:|-----------------:|---------------:|--------------:|
| Champions      |        366 |        253.13 |       92644.7 |            10.72 |             5.16 |            3.3 |          14.9 |
| Leales         |       2560 |        100.96 |      258454   |            31.47 |             1.79 |           23.2 |          41.6 |
| Potenciales    |       3479 |         49.05 |      170632   |            60.12 |             1.19 |           31.5 |          27.5 |
| En riesgo      |       3206 |         25.28 |       81035.7 |            91.19 |             1.06 |           29   |          13   |
| Perdidos       |       1429 |         13.14 |       18783.4 |           121.72 |             1.02 |           12.9 |           3   |



**Insights estratégicos:**

- **Champions** (3.3% clientes, 14.9% ingreso): gasto medio de €253.13, recencia media de 11 días. Son el motor del negocio.
- **Leales** (23.2% clientes, 41.6% ingreso): gasto medio de €100.96. Candidatos naturales a ascender a Champions con fidelización.
- **Potenciales** (31.5% clientes): el grupo más grande. Gasto medio de €49.05. Una compra más los convertiría en Leales.
- **En riesgo** (29.0% clientes): recencia media de 91 días. Ventana de reactivación todavía abierta.
- **Perdidos** (12.9% clientes): recencia media de 122 días. Solo rentable recuperarlos con campañas de muy bajo coste.


---

## 6. Oportunidades y Riesgos Concretos


### 6.1 Clientes en Riesgo de Fuga de Alto Valor (M≥3, F≥2, R≤2)

- **93 clientes** (0.8%)

- Gasto total del segmento: **€13,029.98** (2.1% del total)

- Gasto medio: €140.11 — 2.5x la media general

- Días desde última compra (media): 103

- Compras previas medias: 3.3


> Son clientes que han demostrado valor pero llevan tiempo inactivos. Una campaña personalizada (descuento 10-15% en sus categorías de compra) debería ser la **acción de mayor ROI** del plan CRO.


### 6.2 Potenciales de 2ª Compra (R≥4, F=1, M≥3)

- **2,188 clientes** (19.8%)

- Gasto medio primera compra: **€72.92**

- Días desde compra (media): 24


> Compraron hace poco, gastaron bien, no han repetido. Mayor probabilidad de conversión a recurrentes con email post-compra (secuencia día 3, 7, 21).


### 6.3 One-Shot Recientes (R≥4, F=1)

- **3,764 clientes** (34.1%)

- Gasto medio: €48.41


> Incluso con una tasa de conversión del 15% a 2ª compra se generarían ~564 nuevos recurrentes.


---

## 7. Insights Estratégicos


### Sobre la Estructura del Negocio

1. **Hiperdependencia del segmento premium**: el top 20% de clientes genera el 58.9% del ingreso. Perder clientes Champions tiene impacto desproporcionado.
2. **Base mayoritariamente one-shot**: el 78.8% solo ha comprado una vez. El negocio capta tráfico bien pero no fideliza — el LTV real está muy por debajo del potencial.
3. **La recencia sola no predice el valor**: un cliente R=5 con M=1 apenas vale €10. El valor real emerge de la combinación R+F+M alta.
4. **Pareto amplificado**: los Champions son solo el 3.3% de clientes pero aportan el 14.9% del ingreso — más concentrado que el 80/20 clásico.

### Sobre el Comportamiento de Compra

5. **La 2ª compra es el multiplicador clave**: los clientes con F=2 gastan ~4x más que F=1. Cada euro invertido en conseguir la 2ª compra tiene el mayor retorno potencial.
6. **Ticket medio estable entre segmentos**: la diferencia de gasto total entre Champions y Potenciales se explica por frecuencia, no por ticket unitario. El ticket medio del cosméticos es estable (~€10-15/producto).
7. **Ventana de fidelización estrecha**: el análisis de cohortes muestra que el 90% de clientes ya no está activo en el 2º mes. La acción post-primera compra debe ser inmediata.
8. **Clientes de alto valor monetario en riesgo**: 93 clientes con M≥3 y F≥2 llevan >90 días sin comprar. Ingreso acumulado en riesgo: €13,030.


---

## 8. Acciones CRO Recomendadas por Segmento


| Segmento | Tamaño | % Ingreso | Objetivo | Acción Principal | Canal | Métrica de Éxito |
|---|---|---|---|---|---|---|
| **Champions** | 366 | 14.9% | Retención + Ticket | Programa VIP: early access, envío gratuito, beneficios exclusivos | Email + push | Tasa repetición >80% |
| **Leales** | 2,560 | 41.6% | Ascenso a Champions | Cross-sell de categorías adyacentes + bundling | Email segmentado | % que asciende en 90 días |
| **Potenciales** | 3,479 | 27.5% | 2ª compra | Secuencia email post-compra (día 3, 7, 21) con recomendaciones personalizadas | Email automation | Tasa 2ª compra en 60 días |
| **En riesgo** | 3,206 | 13.0% | Reactivación | Campaña 'te echamos de menos' con descuento 10-15% en categorías favoritas | Email + retargeting | Tasa reactivación en 30 días |
| **Perdidos** | 1,429 | 3.0% | Win-back selectivo | Email bajo coste solo si gasto previo >p50 | Email | ROI > 3x |



### Acciones Transversales

| Acción | Palanca | Impacto Estimado |
|---|---|---|
| Sistema de recomendación personalizado por segmento RFM | Ticket medio | Alto |
| Flujo de onboarding post-primera compra (serie 3-7-21 días) | Frecuencia | Muy alto |
| Programa de puntos/fidelización para Leales y Champions | Frecuencia + retención | Alto |
| Campaña reactivación 'alto valor dormido' (93 clientes, €13,030 en juego) | Retención | Muy alto |
| Análisis de cohortes mensual automatizado | Seguimiento LTV | Estratégico |



---

## 9. Priorización de Acciones


### Corto Plazo (0-30 días)

1. **Campaña reactivación alto valor dormido** — 93 clientes, €13,030 de ingreso potencial. Canal: email personalizado + retargeting.
2. **Secuencia post-compra para one-shot recientes (R≥4)** — 3,764 clientes. Conversión al 15% → 564 nuevos recurrentes.

### Medio Plazo (30-90 días)

3. **Programa VIP para Champions** (366 clientes) — proteger el núcleo del negocio con beneficios exclusivos.
4. **Activación de Leales** — 2,560 clientes con potencial de ascenso. Cross-sell basado en historial de categorías.

### Largo Plazo (90+ días)

5. **Sistema de recomendación personalizado** por segmento RFM.
6. **Dashboard RFM en tiempo real** para detectar migraciones de segmento.
7. **A/B testing de incentivos de reactivación** para calibrar el descuento óptimo.


---

_Análisis basado en 11,040 clientes únicos  ·  Ingreso total analizado: €621,549.60_
