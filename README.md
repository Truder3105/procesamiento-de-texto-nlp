# Procesamiento de Texto — Laboratorio NLP (Semanas 4-6)

Repositorio de laboratorio para la asignatura **Inteligencia Artificial / Procesamiento de Lenguaje Natural**, correspondiente al informe escrito **"Procesamiento de texto"**.

Aplica, con un corpus de comentarios de YouTube (inspirado en el dataset [YouTube Statistics](https://www.kaggle.com/datasets/advaypatil/youtube-statistics) de Kaggle), los siguientes procesos:

**NLP clásico:** Normalización de texto · Stopwords · Stemming · Lematización · Part-of-Speech (POS) Tagging · Parsing · Named Entity Recognition (NER)

**Representación y minería:** Term Frequency (TF) · Inverse Document Frequency (IDF/TF-IDF) · Text Mining · Sentence Similarity · Text Classification

**Modelos de Lenguaje Grande (LLM):** Generación de texto con LLM · Text Generation (estrategias de decodificación) · Question Answering · Summarization · Translation

## Contenido del repositorio

```
├── notebooks/
│   └── Procesamiento_de_Texto_NLP.ipynb   # Notebook principal (Google Colab)
├── informe/
│   └── Procesamiento_de_texto.pdf          # Informe escrito final
├── requirements.txt                        # Dependencias del proyecto
└── README.md
```

## Cómo ejecutar

### Opción recomendada: Google Colab
1. Abrir [Google Colab](https://colab.research.google.com/).
2. `Archivo → Abrir notebook → GitHub`, pegar la URL de este repositorio y seleccionar `notebooks/Procesamiento_de_Texto_NLP.ipynb`.
3. Ejecutar las celdas en orden (`Entorno de ejecución → Ejecutar todas`). Las celdas basadas en `transformers` (LLM) descargan modelos de Hugging Face Hub la primera vez, por lo que requieren conexión a internet.

### Opción local
```bash
git clone https://github.com/TU-USUARIO/procesamiento-de-texto-nlp.git
cd procesamiento-de-texto-nlp
pip install -r requirements.txt
python -m spacy download es_core_news_sm
jupyter notebook notebooks/Procesamiento_de_Texto_NLP.ipynb
```

## Caso de aplicación

El corpus y el análisis de resultados se orientan al proyecto de curso **"Estadísticas de YouTube"**, cuyo objetivo es predecir el desempeño de un video (likes/vistas) a partir del texto de sus comentarios. Este laboratorio construye y valida, paso a paso, el pipeline de NLP necesario para ese modelo: desde la limpieza del texto hasta la clasificación de sentimiento y el uso de LLM para tareas avanzadas (resumen, QA, generación).

## MLOps

Siguiendo las pautas del curso, el proyecto contempla:
- **Manejo de datos:** dataset versionado en este repositorio; para el proyecto final se recomienda versionarlo con DVC o Git LFS.
- **Modelo en la nube:** despliegue del clasificador/embeddings como endpoint (p. ej. Hugging Face Inference Endpoints, AWS SageMaker o Google Cloud Vertex AI) consumible por API.
- **Monitoreo:** registro de métricas de desempeño (accuracy, drift de datos) en el tiempo.

## Librerías utilizadas

`nltk` · `spacy` (+ `displaCy`) · `scikit-learn` · `pandas` · `gensim` · `transformers` (Hugging Face) · `wordcloud` · `matplotlib`

## Referencias

- Cohere LLM University — [What is Similarity Between Sentences?](https://cohere.com/llmu/what-is-similarity-between-sentences)
- Cohere LLM University — [What Are Word and Sentence Embeddings?](https://cohere.com/llmu/sentence-word-embeddings)
- Stanford CS224N — [NLP with Deep Learning, Lectures 12-14](https://www.youtube.com/playlist?list=PLoROMvodv4rMFqRtEuo6SGjY4XbRIVRd4)
- Kaggle — [YouTube Statistics Dataset](https://www.kaggle.com/datasets/advaypatil/youtube-statistics)

## Autor

_(Nombre del estudiante) — (Curso) — (Universidad)_
