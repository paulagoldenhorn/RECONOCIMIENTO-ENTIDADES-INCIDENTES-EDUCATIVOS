# Proyecto de Procesamiento de Lenguaje Natural
Trabajo Práctico Final de la materia Procesamiento de Lenguaje Natural.

El objetivo del trabajo es entrenar y evaluar modelos de Reconocimiento de Entidades Nombradas (NER) para extraer automáticamente información estructurada sobre incidentes en aulas y entornos educativos. A partir de ejemplos de mensajes de docentes en lenguaje natural, los modelos identifican las siguientes entidades:
- **OBJETO**: Elemento físico afectado.
- **PROBLEMA**: Falla o incidente reportado.
- **LUGAR**: Ubicación del incidente.

Tareas realizadas:
- **Dataset**: construcción de ejemplos anotados manualmente y aumentados con herramientas de IA. División en conjuntos de entrenamiento, desarrollo y validación.
- **Modelado**: entrenamiento de tres modelos para comparar dos enfoques, entrenamiento desde cero vs. Aprendizaje por Transferencia:
  - **Fine-tuning spaCy `es_core_news_lg`**: modelo neuronal de spaCy versión grande en español (con embeddings estáticos preentrenados).
  - **Fine-tuning spaCy `es_core_news_sm`**: modelo neuronal de spaCy versión pequeña en español (sin embeddings preentrenados).
  - **Entrenamiento CRF**: modelo probabilístico de Campos Aleatorios Condicionales de scikit-learn.
- **Evaluación**: curvas de entrenamiento, métricas de desarrollo vs. validación (Precision, Recall, F1-score), análisis de errores (Falsos Negativos y Falsos Positivos).

Métricas obtenidas:
<img width="1789" height="495" alt="metricas" src="https://github.com/user-attachments/assets/b2b718cf-ffa0-4382-9406-e12649e2928a" />

Distribución de errores:
<img width="1590" height="886" alt="errores" src="https://github.com/user-attachments/assets/2fbbca15-71d8-46af-97ef-5e280c66ecba" />
