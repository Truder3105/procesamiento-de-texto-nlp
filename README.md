# Procesamiento de Texto — Laboratorio NLP (Semanas 4-6)

Repositorio de laboratorio para la asignatura **Procesamiento de Lenguaje Natural - EIAIIPA2026_2 - CAD2202023206**, correspondiente al informe escrito **"Tarea Informe Procesamiento de texto"**.

Aplica, sobre un corpus de comentarios de YouTube (inspirado en el dataset [YouTube Statistics](https://www.kaggle.com/datasets/advaypatil/youtube-statistics) de Kaggle), los procesos de NLP clásico y de Modelos de Lenguaje Grande (LLM) que se listan a continuación.

---

## Temas cubiertos

**NLP clásico**
- Normalización de texto
- Stopwords
- Stemming
- Lematización
- Part-of-Speech (POS) Tagging
- Parsing
- Named Entity Recognition (NER)

**Representación y minería**
- Term Frequency (TF)
- Inverse Document Frequency (IDF) / TF-IDF
- Text Mining
- Sentence Similarity
- Text Classification

**Modelos de Lenguaje Grande (LLM)**
- Generación de texto con LLM
- Text Generation (estrategias de decodificación)
- Question Answering
- Summarization
- Translation

---

## Contenido del repositorio

```
procesamiento-de-texto-nlp/
├── notebooks/
│   └── Procesamiento_de_Texto_NLP.ipynb   ← Notebook principal (Google Colab)
├── informe/
│   └── Procesamiento_de_texto.pdf         ← Informe escrito final
├── requirements.txt                       ← Dependencias del proyecto
└── README.md
```

---

## Caso de aplicación

El corpus y el análisis de resultados se orientan al proyecto de curso **"Estadísticas de YouTube"**, cuyo objetivo es predecir el desempeño de un video (likes/vistas) a partir del texto de sus comentarios. Este laboratorio construye y valida, paso a paso, el pipeline de NLP necesario para ese modelo: desde la limpieza del texto hasta la clasificación de sentimiento y el uso de LLM para tareas avanzadas (resumen, QA, generación).

## MLOps

Siguiendo las pautas del curso, el proyecto contempla:

- **Manejo de datos:** dataset versionado en este repositorio; para el proyecto final se recomienda versionarlo con DVC o Git LFS.
- **Modelo en la nube:** despliegue del clasificador/embeddings como endpoint (p. ej. Hugging Face Inference Endpoints, AWS SageMaker o Google Cloud Vertex AI) consumible por API.
- **Monitoreo:** registro de métricas de desempeño (accuracy, drift de datos) en el tiempo.

## Librerías utilizadas

`nltk` · `spacy` (+ `displaCy`) · `scikit-learn` · `pandas` · `gensim` · `transformers` (Hugging Face) · `sentence-transformers` · `wordcloud` · `matplotlib`

## Referencias

- Cohere LLM University — [What is Similarity Between Sentences?](https://cohere.com/llmu/what-is-similarity-between-sentences)
- Cohere LLM University — [What Are Word and Sentence Embeddings?](https://cohere.com/llmu/sentence-word-embeddings)
- Stanford CS224N — [NLP with Deep Learning, Lectures 12-14](https://www.youtube.com/playlist?list=PLoROMvodv4rMFqRtEuo6SGjY4XbRIVRd4)
- Kaggle — [YouTube Statistics Dataset](https://www.kaggle.com/datasets/advaypatil/youtube-statistics)

## Autor

_(Julian Esteban Ballesteros Ortiz, Juan Diego Walteros Cortes) — (PROCESAMIENTO DE LENGUAJE NATURAL - EIAIIPA2026_2 - CAD2202023206) — (Universidad de Cundinamarca)_
