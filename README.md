# alzheimer-project-classification

# Problema y estructura del Dataset

## Detección de Alzheimer a través de Imágenes

La enfermedad del Alzheimer es la causa más frecuente de demencia. Este proceso neurodegenerativo, de causa incierta y patogenia parcialmente conocida, afecta preferentemente a personas mayores de 65 años, ocasionando en la mayoría de los casos una pérdida progresiva de un tipo muy selectivo de memoria. Constituye la forma más frecuente de demencia. 

Un diagnóstico temprano puede ser clave para manejar los síntomas y planificar un tratamiento. Este proyecto busca clasificar imágenes de resonancia magnética cerebral (MRI) en 4 categorías, basadas en el grado de demencia:

- **Mild Demented (0):** Etapa leve de demencia.
- **Moderate Demented (1):** Etapa moderada de demencia.
- **Non Demented (2):** Sin indicios de demencia.
- **Very Mild Demented (3):** Etapa muy leve de demencia.

La meta es desarrollar un modelo de aprendizaje profundo capaz de distinguir estas clases.

---

## Estructura del Dataset

El dataset está dividido en dos partes:

- **Train split:** Para entrenar el modelo.
- **Test split:** Para evaluar el modelo.

Ambas particiones están almacenadas en formato **Parquet**, que es un formato columnar optimizado para procesamiento de datos, pero no para imágenes. Por lo tanto, antes de entrenar el modelo, necesitamos transformar el dataset para poder utilizarlo.

### Contenido de los archivos

Cada archivo Parquet contiene:

- **Imágenes:** En un formato serializado.
- **Etiquetas:** Indican a qué clase pertenece cada imagen (`0`, `1`, `2` o `3`).

El dataset consiste en imágenes MRI del cerebro, etiquetadas en 4 categorías:

- **`0`:** Mild_Demented  
- **`1`:** Moderate_Demented  
- **`2`:** Non_Demented  
- **`3`:** Very_Mild_Demented  

---

## Información del Dataset

### Train split
- **Name:** `train`
- **Tamaño:** 22,560,791.2 bytes
- **Número de ejemplos:** 5,120

### Test split
- **Name:** `test`
- **Tamaño:** 5,637,447.08 bytes
- **Número de ejemplos:** 1,280

- **Tamaño total de descarga:** 28,289,848 bytes  
- **Tamaño total del dataset:** 28,198,238.28 bytes  

---

## Cita

Si utilizas este dataset en tus investigaciones o aplicaciones en medicina de la salud, te solicitamos amablemente que cites la siguiente publicación:

```bibtex
@dataset{alzheimer_mri_dataset,
  author = {Falah.G.Salieh},
  title = {Alzheimer MRI Dataset},
  year = {2023},
  publisher = {Hugging Face},
  version = {1.0},
  url = {https://huggingface.co/datasets/Falah/Alzheimer_MRI}
}
