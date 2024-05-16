# MODELOS GRANDES DE LENGUAJE (LLM)
Repositorio de la materia LLM de la Especialización en IA

Alumno: Leandro Albachiaro

mail: leandroalbachiaro@gmail.com

## Introducción

El objetivo de este proyecto es implementar un modelo capaz de detectar mensajes de texto SPAM para proteger a los usuarios de comunicaciones no deseadas y potencialmente peligrosas. Para esto se utilizará DistilBERT, una versión compacta y eficiente del modelo BERT, pre-entrenado para tareas de procesamiento del lenguaje natural (NLP).

## Desarrollo

- **Preparación de datos:** Se realiza un análisis exploratorio del dataset, el cual contiene una colección de 5572 mensajes de texto etiquetados como SPAM o legítimos. [SMS Spam Collection Dataset | Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

- **Carga del modelo pre-entrenado de DistilBERT:** Se utiliza la biblioteca `transformers` de Hugging Face para cargar el modelo pre-entrenado de DistilBERT y su tokenizador correspondiente.

- **Tokenización de mensajes:** Se tokenizan los mensajes de texto utilizando el tokenizador de DistilBERT.

- **Entrenamiento del modelo:** Se define una arquitectura de clasificación de secuencias utilizando DistilBERT como base y se ajustan los pesos del modelo utilizando los datos de entrenamiento. Durante el entrenamiento, se ajustan los parámetros del modelo para minimizar la función de pérdida de entropía cruzada (Cross-Entropy Loss), que mide la discrepancia entre las predicciones del modelo y las etiquetas reales.

- **Evaluación del modelo:** Una vez entrenado el modelo, se evalúa su rendimiento utilizando datos de prueba previamente no vistos. Se calculan métricas como precisión y recall para medir la capacidad del modelo para distinguir entre mensajes de texto SPAM y legítimos.

## Conclusiones

- **Precisión y recall significativos:** Los resultados muestran la capacidad del modelo para identificar mensajes de spam con una precisión y recall significativos.
  
- **Viabilidad y eficacia de DistilBERT:** A pesar de ser un modelo más pequeño y compacto, se demostró con éxito la viabilidad y eficacia de utilizar DistilBERT para la detección de spam en mensajes de texto.
