# Proyecto de Procesamiento de Lenguaje Natural

Sistema de Reconocimiento de Entidades Nombradas (NER) aplicado a la gestión de incidentes en aulas. El objetivo es, a partir de mensajes en lenguaje natural enviados por docentes, extraer automáticamente información estructurada acerca del incidente:
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
