# Memoria viva para futura redacción en LaTeX

> Este archivo sirve como guía para mantener el contexto del posible LaTeX a entregary sugerir una estructura. La idea es crear otro md donde vayamos escribiendo el LaTeX final. Todo ese documento lo escribimos en formato LaTeX. Todo ese contenido me lo aportas tú a traves de un widget para que yo solo tenga que copiar y pegar, manteniendo la consistencia, coherencia y no redundancia de la memoria. Para ello, tienes acceso a la memoria constantemente.

---

## Título provisional
Clasificación binaria del abandono de clientes en telecomunicaciones mediante técnicas de selección de variables y redes neuronales

## 1. Introducción
### Idea base
Este trabajo aborda un problema de clasificación binaria en el contexto de abandono de clientes en una empresa de telecomunicaciones. El objetivo es predecir si un cliente abandonará el servicio a partir de un conjunto de variables descriptivas relacionadas con patrones de uso, planes contratados y actividad con el servicio de atención.

### Cosas que habrá que contar aquí
- contexto del problema,
- utilidad empresarial de anticipar churn,
- descripción general del dataset,
- estructura del trabajo.

---

## 2. Descripción del conjunto de datos
### Pendiente de completar
- número de filas y columnas,
- tipo de variables,
- variable objetivo,
- breve comentario sobre variables categóricas, numéricas e identificativas.

### Posibles observaciones
- `V4` podría ser una variable identificativa y no predictiva.
- Puede haber relaciones muy fuertes entre minutos y costes.
- Hay variables binarias asociadas a planes contratados.

---

## 3. Análisis y depuración de datos
### Qué habrá que justificar
- tratamiento de nulos,
- eliminación o conservación de duplicados,
- exclusión de variables no informativas o identificativas,
- codificación de categóricas,
- escalado cuando proceda,
- prevención de fuga de información,
- decisiones específicas según el modelo.

### Texto provisional reutilizable
La fase de depuración y preparación de datos no debe entenderse como un bloque mecánico previo al modelado, sino como una parte esencial del diseño metodológico. Cada técnica empleada en el trabajo exige condiciones distintas sobre la representación de las variables, por lo que el preprocesado se adaptó de forma específica al modelo considerado en cada apartado.

---

## 4. Metodología del apartado 2
### 4.1 Selección de variables mediante RFE con regresión logística
#### Ideas a desarrollar
- por qué usar RFE,
- por qué una regresión logística como estimador base,
- cómo se seleccionaron exactamente 5 variables,
- por qué la selección se hizo solo con entrenamiento.

### 4.2 Red neuronal optimizada en Accuracy
#### Ideas a documentar
- arquitectura/s probadas,
- hiperparámetros,
- procedimiento de búsqueda,
- criterio de selección,
- threshold elegido,
- resultados finales.

### Tabla pendiente
- combinaciones de hiperparámetros probadas,
- accuracy de validación,
- threshold evaluados,
- configuración ganadora.

---

## 5. Metodología del apartado 3
### 5.1 Selección de variables mediante árbol de decisión
#### Ideas a desarrollar
- entrenamiento del árbol,
- criterio de importancia,
- número de variables seleccionadas,
- interpretación de las variables importantes.

### 5.2 Red neuronal optimizada en Recall
#### Ideas a documentar
- arquitectura/s probadas,
- regularización y número de iteraciones,
- criterio de selección basado en recall,
- análisis del threshold,
- resultados finales.

---

## 6. Comparación global de modelos
### Cosas que habrá que incluir
- tabla comparativa de métricas,
- discusión de accuracy vs recall,
- interpretabilidad,
- complejidad,
- sensibilidad al threshold,
- valoración crítica final.

### Texto provisional reutilizable
La comparación entre modelos no debe limitarse a una lectura aislada de una única métrica. En problemas de abandono de clientes, el coste relativo de falsos negativos y falsos positivos puede alterar significativamente la conveniencia práctica de un modelo. Por ello, además de comparar el rendimiento agregado, resulta necesario interpretar el equilibrio entre métricas y el efecto de la elección del umbral de clasificación.

---

## 7. Figuras candidatas
- distribución de la variable objetivo,
- mapa de correlaciones,
- gráfico de importancias del árbol,
- curva de métricas frente a threshold,
- matrices de confusión finales,
- tabla resumen de resultados.

---

## 8. Conclusiones
### Puntos que habrá que responder
- qué modelo fue mejor y bajo qué criterio,
- qué selección de variables resultó más útil,
- qué decisiones metodológicas fueron clave,
- qué limitaciones tiene el enfoque,
- posibles mejoras futuras.

---------------------------------------------- COMIENZO --------------------------

El trabajo se organizó siguiendo un flujo reproducible y progresivo. Antes de ajustar los modelos, se definió una estructura de proyecto versionada y se separaron las fases de carga, análisis exploratorio, depuración, selección de variables, entrenamiento y comparación final. Esta organización permite justificar cada decisión metodológica y evita que el notebook se convierta en una sucesión desordenada de pruebas.
