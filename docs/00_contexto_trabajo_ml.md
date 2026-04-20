# Contexto del trabajo - Machine Learning 2026

## Descripción general
Trabajo individual de **clasificación binaria** orientado a predecir la variable objetivo `Y`, que indica si un cliente de telecomunicaciones abandona el servicio (`Y=1`) o no (`Y=0`).

La evaluación se realiza **exclusivamente** sobre una **memoria en PDF**, autoexplicativa, reproducible y con un máximo de **20 páginas**. El código en Python se entrega aparte para reproducir resultados, pero **no se evalúa directamente**.

## Restricciones importantes
- El trabajo es individual.
- La memoria en PDF debe ser autoexplicativa.
- No se admiten entregas de la memoria en `.ipynb`, `.py` o exportaciones con logs.
- Se debe usar la base de datos proporcionada: `BBDD_ML_TAREA.csv`.
- Hay que explicar la depuración/preparación de datos necesaria para cada técnica.
- La memoria debe priorizar claridad, estructura, justificación metodológica y reproducibilidad.

## Variables del problema
Variables independientes: `V1` a `V20`.
Variable dependiente: `Y`.

### Significado de variables
- `V1`: Estado/región del cliente
- `V2`: Duración de la cuenta con la empresa
- `V3`: Código de área telefónica
- `V4`: Número de teléfono del cliente
- `V5`: Plan internacional contratado (sí/no)
- `V6`: Plan de buzón de voz contratado (sí/no)
- `V7`: Número de mensajes de buzón de voz
- `V8`: Minutos totales de llamadas diurnas
- `V9`: Número de llamadas diurnas
- `V10`: Coste total de llamadas diurnas
- `V11`: Minutos totales de llamadas vespertinas
- `V12`: Número de llamadas vespertinas
- `V13`: Coste total de llamadas vespertinas
- `V14`: Minutos totales de llamadas nocturnas
- `V15`: Número de llamadas nocturnas
- `V16`: Coste total de llamadas nocturnas
- `V17`: Minutos totales de llamadas internacionales
- `V18`: Número de llamadas internacionales
- `V19`: Coste total de llamadas internacionales
- `V20`: Número de llamadas al servicio de atención

## Objetivo del problema
Desarrollar un sistema de clasificación que determine si un cliente está en riesgo de abandono (`Y=1`) basándose en sus patrones de consumo y servicio.

## Cuestiones obligatorias

### 1. Análisis y depuración de datos
Analizar y depurar la base de datos, documentando y justificando:
- transformaciones realizadas,
- técnicas de feature engineering aplicadas,
- motivo de cada proceso,
- cómo contribuye cada proceso al rendimiento de los modelos.

### 2. Regresión logística + RFE + red neuronal (optimizar Accuracy)
1. Aplicar un proceso de **RFE** cuyo modelo base sea una **regresión logística** para seleccionar **5 variables**.
2. Con esas 5 variables, diseñar y ajustar una **red neuronal** optimizada en términos de **Accuracy**.
3. Realizar una **búsqueda paramétrica exhaustiva**.
4. Justificar detalladamente:
   - parametrizaciones probadas,
   - threshold de clasificación elegido,
   - selección final de parámetros y su impacto en el rendimiento.

### 3. Árbol de decisión + variables importantes + red neuronal (optimizar Recall)
1. Entrenar un **árbol de decisión**.
2. Seleccionar las variables más relevantes según la importancia calculada por el modelo.
3. Usar esas variables para construir y ajustar la mejor **red neuronal** en términos de **Recall**.
4. Realizar una **búsqueda paramétrica exhaustiva**.
5. Justificar detalladamente:
   - parametrizaciones probadas,
   - threshold de clasificación elegido,
   - parámetros finales y su influencia.

### 4. Comparación global de modelos
Comparar exhaustivamente los enfoques de los apartados 2 y 3:
- métricas de evaluación,
- ventajas e inconvenientes,
- decisiones metodológicas,
- evaluación crítica final del/los modelo(s) más adecuado(s).

## Criterios implícitos que deben guiar el trabajo
- Reproducibilidad.
- Justificación de decisiones.
- Claridad expositiva.
- Separación entre exploración, entrenamiento y redacción.
- No hacer código por hacer: cada paso debe responder a una necesidad metodológica.

## Filosofía de trabajo para este proyecto
- El notebook debe servir para **aprender**, no solo para obtener resultados.
- Primero se entiende el objetivo, luego se divide en fases, luego en pasos concretos.
- La memoria en LaTeX se va rellenando en paralelo cuando una decisión o resultado ya esté suficientemente consolidado.
- Conviene mantener un archivo vivo con texto en formato casi-LaTeX / pseudo-LaTeX para que luego la memoria final salga con poco esfuerzo.
