# Estructura propuesta del notebook

## 0. Portada del notebook
- Título del trabajo
- Asignatura / módulo
- Objetivo general
- Idea de la estrategia de resolución

## 1. Lectura del enunciado y planificación
### Objetivo
Dejar claro qué pide exactamente el trabajo y cómo se va a abordar.

### Contenido
- Resumen del problema
- Restricciones de entrega
- Preguntas obligatorias
- Plan general por fases

## 2. Carga de librerías y datos
### Objetivo
Leer correctamente la base de datos y comprobar estructura, tipos y dimensión.

### Posibles celdas
- Importaciones
- Carga del CSV
- `head`, `shape`, `info`, `describe`
- Revisión inicial de variable objetivo

## 3. Análisis exploratorio y depuración
### Objetivo
Entender calidad, estructura y riesgos del dataset antes de modelar.

### Subpasos sugeridos
- Detección de nulos
- Detección de duplicados
- Revisión de cardinalidad de variables categóricas
- Identificación de variables potencialmente problemáticas (`V4`, etc.)
- Distribución de la variable objetivo
- Outliers y escalas
- Relaciones obvias o redundancias entre variables de minutos/costes
- Decisiones de preprocesado justificadas

## 4. Preparación metodológica antes de modelar
### Objetivo
Definir cómo se va a separar train/test y qué preprocesado corresponde a cada familia de modelos.

### Subpasos sugeridos
- Separación `X` / `y`
- Train/test split estratificado
- Justificación de variables a eliminar o conservar
- Codificación de variables categóricas
- Escalado cuando proceda
- Idea de pipeline para evitar leakage

## 5. Apartado 2 - RFE con regresión logística + red neuronal orientada a Accuracy
### 5.1 Selección de variables por RFE
- Definir preprocesado compatible con regresión logística
- Ejecutar RFE sobre train
- Seleccionar 5 variables
- Interpretar selección

### 5.2 Red neuronal con esas variables
- Preparar dataset final con las 5 variables
- Definir red neuronal base
- Diseñar espacio de búsqueda paramétrica
- Evaluar en términos de Accuracy
- Analizar curvas / resultados
- Elegir threshold
- Evaluación final

## 6. Apartado 3 - Árbol de decisión + variables importantes + red neuronal orientada a Recall
### 6.1 Árbol de decisión para importancia de variables
- Entrenar árbol
- Obtener importancias
- Elegir subconjunto de variables
- Justificar criterio de corte

### 6.2 Red neuronal con variables importantes
- Preparar conjunto de entrada
- Definir red neuronal base
- Diseñar búsqueda paramétrica exhaustiva
- Optimizar Recall
- Analizar threshold
- Evaluación final

## 7. Comparación global
### Objetivo
Comparar con criterios homogéneos ambos enfoques.

### Posibles comparaciones
- Accuracy
- Recall
- Precision
- F1-score
- ROC-AUC
- Matriz de confusión
- Robustez / interpretabilidad / complejidad
- Ventajas e inconvenientes

## 8. Conclusiones
- Qué enfoque funciona mejor y en qué sentido
- Qué trade-offs aparecen
- Qué decisiones fueron importantes
- Qué limitaciones tiene el trabajo

## 9. Material para memoria
- Fragmentos clave de interpretación
- Tablas resumen
- Figuras candidatas
- Resultados que deben documentarse en LaTeX
